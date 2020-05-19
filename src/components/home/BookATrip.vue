<template>
  <div class="book-a-trip-component">
    <div class="buttons">
      <a href="javascript:void(0)"><img src="@/assets/images/book_plane.svg" /> Book a trip</a>
      <a href="javascript:void(0)"><img src="@/assets/images/book_car.svg" /> Rent a car</a>
    </div>

    <form class="form">
      <b-row no-gutters>
        <b-col cols="4">
          <b-container fluid class="fields-wrap">
            <b-row>
              <b-col cols="12">
                <label class="label">Where</label>
                <b-form-select v-model="location.selected" :options="location.options" class="form-select"></b-form-select>
              </b-col>
            </b-row>
          </b-container>
        </b-col>
        
        <b-col cols="4">
          <b-container fluid class="fields-wrap">
            <b-row class="flex-nowrap">
              <b-col cols="6">
                <label class="label">Start Date</label>
                <label for="start-date" class="text-nowrap">{{ startDate }}</label>
                <b-form-datepicker id="start-date" v-model="startDate" class="hide-date-field"></b-form-datepicker>
              </b-col>
              <b-col cols="6">
                <label class="label">End Date</label>
                <label for="start-date" class="text-nowrap">{{ endDate }}</label>
                <b-form-datepicker v-model="endDate" class="hide-date-field"></b-form-datepicker>
              </b-col>
            </b-row>
          </b-container>
        </b-col>

        <b-col>
          <b-container fluid class="fields-wrap">
            <b-row>
              <b-col cols="12">
                <label class="label">Where</label>
                <b-form-select v-model="travellers.selected" :options="travellers.options" class="form-select"></b-form-select>
              </b-col>
            </b-row>
          </b-container>
        </b-col>
        
        <b-col class="form-actions flex-grow-0">
          <b-container fluid class="fields-wrap">
            <b-row>
              <b-col cols="12">
                <b-button type="button"><img src="@/assets/images/search_icon_black.svg"/></b-button>
              </b-col>
            </b-row>
          </b-container>
        </b-col>

      </b-row>
    </form>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        location:{
          selected: null,
          options: [
            { value: null, text: 'Anywhere in Jordan' },
            { value: 1, text: 'Location 1' },
            { value: 2, text: 'Location 2' },
            { value: 3, text: 'Location 3' },
            { value: 4, text: 'Location 4' }
          ]
        },
        startDate: "2020-01-01",
        endDate: "2020-02-10",
        travellers:{
          selected: 3,
          options: [
            { value: null, text: 'No Traveller' },
            { value: 1, text: '1 traveller' },
            { value: 2, text: '2 travellers' },
            { value: 3, text: '3 travellers' },
            { value: 4, text: '4 travellers' }
          ]
        }
      }
    }
  }
</script>
<style lang="scss">
.book-a-trip-component{
  position: relative;
  z-index: 16;

  .buttons{
    position: absolute;
    bottom: 100%;
    margin-bottom: 25px;
    display: flex;
    align-items: center;

    a{
      color: #fff;
      font-size: 16px;
      font-weight: 600s;
      text-transform: uppercase;
      margin-right: 35px;
      display: flex;
      align-items: center;
      white-space: nowrap;

      img{margin-right: 8px;}

      &:hover{text-decoration: none;}
    }
  }

  .form{
    background: #fff;
    border-radius: 4px;
    overflow: hidden;
    box-shadow: 3px 3px 10px rgba(0,0,0,0.09);
    font-size: 24px;
    font-weight: 300;

    > .row > div{
      border-right: 1px solid var(--fourth);

      &:last-child{border-right: 0;}
    }
    .fields-wrap{
      padding: 30px 15px;
      max-width: 90%;
    }
    .label{
      font-size: 16px;
      font-weight: bold;
      text-transform: uppercase;
      line-height: 1;
    }
    .form-control{
      font-size: inherit;
      font-weight: inherit;
      outline: none;
    }
    .form-select{
      font-size: inherit;
      font-weight: inherit;
      display: block;
      outline: none;
      box-shadow: none;
      margin: 0 -10px;
      padding: 0 10px;
      border: 0;
      height: auto;
      line-height: 1;
      min-height: 0;
    }

    .form-actions{
      background: var(--secondary);
      display: flex;
      justify-content: center;
      align-items: center;
      min-width: 102px;

      .fields-wrap{
        padding: 0;
        width: 100px;
        text-align: center;
      }
      .btn{
        background: transparent;
        border-radius: 0;
        border: 0;
        width: auto;
        height: auto;
        padding: 0;
        margin: 0;
      }
    }
  }
}
.home-view .book-a-trip-component{
  -webkit-transform: translateY(-50%);
  -moz-transform: translateY(-50%);
  transform: translateY(-50%);
}
</style>