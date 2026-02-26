<script setup>

import LayoutNav from './components/LayoutNav.vue';
import LayoutFooter from './components/LayoutFooter.vue';
import LayoutHeader from './components/LayoutHeader.vue';
import LayoutFixed from './components/LayoutFixed.vue'; 

//触发获取列表导航
import { useCategoryStore } from '@/stores/category';
import {onMounted} from 'vue'

const categoryState = useCategoryStore()
onMounted(() => categoryState.getCategory())

</script>

<<template>
    <LayoutFixed />
    <LayoutNav />
    <LayoutHeader />
    <RouterView />
    <LayoutFooter />
</template>>

