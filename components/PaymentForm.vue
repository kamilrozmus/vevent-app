<template>
  <div class="content">
    <form class="form" action="#">
      <h3>Select additional services</h3>
      <span class="title-description">Services</span>
      <div class="checkboxes mt-2">
        <input type="checkbox" name="myCheckBox" id="checkbox">
        <label for="checkbox">Massage and Spa
          <span style="float: right">+$50.00</span>
        </label>
        <input type="checkbox" name="myCheckBox" id="checkbox1">
        <label for="checkbox1">Airport pickup
          <span style="float: right">+$20.00</span>
        </label>
        <input type="checkbox" name="myCheckBox" id="checkbox2">
        <label for="checkbox2">Breakfast
          <span style="float: right">+$15.00</span>
        </label>
      </div>

      <span class="title-description">Payment for booking</span>
      <select class="mt-2">
        <option>Credit or debit Visa card</option>
        <option>Paypal</option>
        <option>Bitcoin</option>
      </select>
      <input 
        type="tel" 
        inputmode="numeric" 
        pattern="[0-9\s]{13,19}" 
        autocomplete="cc-number" 
        maxlength="19" 
        placeholder="xxxx xxxx xxxx xxxx"
      >
      <div class="card-details">
        <input 
          type="text" 
          placeholder="Expiration"
          class="mr-2"
        >
        <input 
          type="number"
          pattern="[0-9\s]{3}"
          placeholder="CVV"
        >
      </div>
    </form>
  </div>
</template>
<style lang="scss" scoped>

h3 {
  display: flex;
  justify-content: center;
}

.content {
  display: flex;
  justify-content: center;
  flex-direction: column;
  max-width: 30em;
  margin: 0 auto 2em;
}

.checkboxes {
  display: flex; 
  flex-direction: column;
}

.title-description {
  font-size: .8em;
  color: $description;
}

label {
  border: 1px solid $gray;
  padding: .7em 1em;
  border-radius: .4em;
  font-weight: bold;
  font-size: .9em;
}

label::before{
  width: 20px;
  height: 20px;
  border: 1px solid $checkbox;
  content: ' ';
  border-radius: 10px;
  float: left;
  margin:0 10px;
  cursor: pointer;
}

label::after{
  display: none;
  transform: translate(1.05em, -1.1em);
  content: '';
  color: $checkbox;
  position: absolute;
  width: 10px;
  height: 10px;
  background-color: $checkbox;
  border-radius: 5px;
  cursor: pointer;
}

input[type=checkbox]:checked + label::after {
  display: block;
}
input[type=checkbox] {
  display:none;
}

.card-details {
  display: flex;
}

input, select {
  width: 100%;
  border: 1px solid $gray;
  padding: .7em 1em;
  border-radius: .4em;
  font-weight: bold;
  font-size: .9em;
  margin-top: .5em;
} 
</style>
