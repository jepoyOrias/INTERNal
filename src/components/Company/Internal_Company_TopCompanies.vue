<template>
    <ul class="list-unstyled">
        <li v-for="(company, index) in companies" :key="index">
            <div class="card border-0 py-2 h-100">
                <div class="card-header border-0 fw-bold text-success bg-white d-flex gap-3">
                    <img v-if="handleImageError(company.image, index)" ref="image" :src="company.image" alt="Image" />
                    <div class="rounded-1 p-3 img text-white text-uppercase"
                        :style="`background-color: ${randomColors[index]} !important;`" v-else>
                        {{ company.name[0]}}
                    </div>
                    <div>
                        <h6 class="fw-bold text-primary">{{ company.name }}</h6>
                        <div class="fw-normal text-secondary">{{ company.headquarter }}</div>
                        <div class="fw-normal text-secondary fw-semibold"> INDUSTRY: <span class="fw-normal">{{ company.industry }}</span></div>
                    </div>
                </div>
            </div>
        </li>
    </ul>
</template>
  
<script lang="ts">
import { computed, defineComponent, PropType, ref } from 'vue';
import Company from '@/types/Company';

export default defineComponent({
    props: {
        companies: {
            required: true,
            type: Array as PropType<Company[]>,
        },
    },
    setup() {
        const randomColors = ref<string[]>([]);

        const handleImageError = (image: string | null, index: number) => {
            if (image !== null) {
                return true;
            }
            randomColors.value[index] = generateRandomColor();
            return false;
        };

        const generateRandomColor = ()=>{
      // Generate a random hex color
            const letters = '0123456789ABCDEF';
            let color = '#';
            for (let i = 0; i < 6; i++) {
                color += letters[Math.floor(Math.random() * 16)];
            }
            return color;
    }

        return { handleImageError, generateRandomColor, randomColors };
    },
});
</script>
  
<style scoped>
ul li {
    margin-bottom: 20px;
}

ul li .card {
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.12);
}

ul li .card-header img,
div.img {
    width: 50px;
    height: 50px;
}

div.img {
    display: flex;
    justify-content: center;
    align-items: center;
}</style>
  