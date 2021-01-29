<template>
  <div>
    <v-container>
      <h2 class="my-5 text-right">الشاليهات</h2>
      <shaleh-card></shaleh-card>

        <h2 class="my-7 text-right">الحجز</h2>
      <shaleh-reservation></shaleh-reservation>
    </v-container>
  </div>
</template>

<script>
import shalehcard from '@/components/shalehcard';
import reservation from '@/components/reservation';

export default {
  components: {
    'shaleh-card': shalehcard,
    'shaleh-reservation': reservation
  },
  data(){
    return{

    }
  }
}
</script>
