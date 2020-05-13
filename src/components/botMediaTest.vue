<template>
  <div class="hello">
    <p>one + two = {{ sum }}</p>
  </div>
</template>

<script>
export default {
    name: "botMediaTest",
    data() {
        return {
            three: 0
        };
    },
    props: {
        one: Number,
        two: Number
    },
    computed: {
        sum: {
            get() {
                return this.one + this.two + this.three;
            },
            set(value) {
                this.three = value;
            }
        }
    },
    methods: {
        increment() {
            this.sum = this.three + 1;
        }
    }
};
</script>

<style lang="scss">
    @import '../assets/mixins.scss';

    .hello {
        @include breakpoint48;
    }
</style>
