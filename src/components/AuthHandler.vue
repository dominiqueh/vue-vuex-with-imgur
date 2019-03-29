<template>
    <div>
        Please wait...
    </div>
</template>

<script>
import { mapActions } from 'vuex';

export default {
    name: 'AuthHandler',
    // ALLOWS ACCESS TO ACTIONS
    methods: mapActions(['finalizeLogin']),
    created() {
      this.finalizeLogin(window.location.hash)
    }
};
</script>