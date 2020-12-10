<template>
  <div>
    <div class="header">
      <div>
        <img src="@/assets/Icon.png" style="size: 20px">
      </div>
      <div>
        <img src="@/assets/avatar.png" style="size: 20px">
      </div>
    </div>
    <PaymentForm />
      <div class="stepper stepper--horizontal">
        <div class="col current">
          <span class="step-number">
            <img src="@/assets/unseen-circle.png" class="mt-2">
          </span>
          <div class="step-title">
            <span>Booking</span>
          </div>
        </div>
        <div class="col">
          <span class="step-number">
            <img src="@/assets/unseen-circle.png" class="mt-2">
          </span>
          <div class="step-title">
            <span>Checkout</span>
          </div>
        </div>
        <div class="d-flex" style="transform: translateY(30px)">
          <span class="step-number">
            <img src="@/assets/visited-circle.png" class="mr-2">
          </span>
          <div class="step-title last">
            <span>Confirm</span>
          </div>
        </div>
      </div>
      <div class="footer">
      <div>
        <button>Back</button>
      </div>
      <div>
        <button class="next">Next</button>
      </div>
    </div>
  </div>
</template>
<script>

import PaymentForm from '@/components/PaymentForm.vue'

export default {
  name: 'PaymentPage',
  components: { PaymentForm }
}
</script>
<style lang="scss" scoped>

body {
  font-family: 'Source Sans Pro', sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0;
  min-height: 100vh;
}

.header {
  display: flex;
  justify-content: space-between;
}

.stepper {
	font-family: 'Roboto', sans-serif;
	display: flex;
	width: 90%;
	margin: auto;
	.col {
		order: 0;
	}
}

.stepper.stepper--horizontal {
  display: flex;
	flex-direction: row;
	flex-wrap: nowrap;
	justify-content: center;
	align-content: center;
  height: 100%;

	.col {
		flex: 0 1 33.3%;
		align-self: auto;
    padding: 20px 0;
    
		span.step-number {
			float: left;
			display: inline-block;
			color: #fff;
			border-radius: 50px;
    }
    
		.step-title {
			color: black;
			padding: 10px 5px 5px 12px;
			display: inline-block;
			width: 85%;
    }
    
		.step-title:after {
			content: "";
			border-bottom: solid 1px #ccc;
			display: inline-block;
			width: 90%;
			float: right;
			position: relative;
			top: -10px;
    }
    
		.step-title span {
			background-color: #fff;
			display: inline-block;
			position: relative;
			z-index: 9;
			padding-right: 4px;
		}
	}

  .step-title.last::after {
    display: none;
  }

	.col.current {
		.step-title {
			color: #000;
		}
	}
}

.footer {
  margin-top: 4em;
  display: flex;
  justify-content: space-between;
}

button {
  font-size: .9em;
  padding: .35em 1.7em .6em;
  border-radius: .7em;
  border: none;
  transition: .5s;
  cursor: pointer;
  &:hover {
    transform:scale(1.1);
  }
  &.next {
    background: $red-primary;
    color: $white;
  }
}
</style>
