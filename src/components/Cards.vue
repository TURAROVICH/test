<template>
    <div class="main">
        <Card v-for="(i,k) in res" :key="k"
        :name="i.relationships.attributes"
        :des="i.attributes.title"
        :rooms="i.attributes.rooms"
        :area="i.attributes.area"
        :unit="i.attributes.unit"
        :address="i.attributes.address"
        />
    </div>
</template>


<script>
import Card from './Card.vue'
export default {
    data:()=>({
        res:null
    }),
     mounted(){
    
     this.res =  {
    "response": [
      {
        "type": "flat",
        "id": 1,
        "attributes": {
          "title": "3-х комнатная на Минской",
          "rooms": 3,
          "address": {
            "city": "Tyumen",
            "street": "Минская",
            "house": "3a",
            "room": "123"
          },
          "area": 134,
          "unit": "квм"
        },
        "relationships": {
          "type": "agent",
          "id": 2,
          "attributes": {
            "first_name": "Василий",
            "last_name": "Дроздов",
            "middle_name": "Михайлович"
          }
        }
      },
      {
        "type": "flat",
        "id": 2,
        "attributes": {
          "title": "1 комнатная на Барабаинской",
          "rooms": 2,
          "address": {
            "city": "Tyumen",
            "street": "Барабинская",
            "house": "12",
            "room": "45"
          },
          "area": 34,
          "unit": "квм"
        },
        "relationships": {
          "type": "agent",
          "id": 10,
          "attributes": {
            "first_name": "Михаил",
            "last_name": "Иванов",
            "middle_name": "Демидович"
          }
        }
      },
      {
        "type": "flat",
        "id": 3,
        "attributes": {
          "title": "Квартира Ленина",
          "rooms": 4,
          "address": {
            "city": "Tyumen",
            "street": "Ленина",
            "house": "134",
            "room": "24"
          },
          "area": 134,
          "unit": "квм"
        },
        "relationships": {
          "type": "agent",
          "id": 44,
          "attributes": {
            "first_name": "Степан",
            "last_name": "Карачаев",
            "middle_name": "Иванович"
          }
        }
      },{
        "type": "flat",
        "id": 3,
        "attributes": {
          "title": "Квартира Ленина",
          "rooms": 4,
          "address": {
            "city": "Tyumen",
            "street": "Ленина",
            "house": "134",
            "room": "24"
          },
          "area": 134,
          "unit": "квм"
        },
        "relationships": {
          "type": "agent",
          "id": 44,
          "attributes": {
            "first_name": "Степан",
            "last_name": "Карачаев",
            "middle_name": "Иванович"
          }
        }
      },
      {
        "type": "flat",
        "id": 3,
        "attributes": {
          "title": "Квартира Ленина",
          "rooms": 4,
          "address": {
            "city": "Tyumen",
            "street": "Ленина",
            "house": "134",
            "room": "24"
          },
          "area": 134,
          "unit": "квм"
        },
        "relationships": {
          "type": "agent",
          "id": 44,
          "attributes": {
            "first_name": "Степан",
            "last_name": "Карачаев",
            "middle_name": "Иванович"
          }
        }
      },
      {
        "type": "flat",
        "id": 3,
        "attributes": {
          "title": "Квартира Ленина",
          "rooms": 4,
          "address": {
            "city": "Tyumen",
            "street": "Ленина",
            "house": "134",
            "room": "24"
          },
          "area": 134,
          "unit": "квм"
        },
        "relationships": {
          "type": "agent",
          "id": 44,
          "attributes": {
            "first_name": "Степан",
            "last_name": "Карачаев",
            "middle_name": "Иванович"
          }
        }
      },
      {
        "type": "flat",
        "id": 3,
        "attributes": {
          "title": "Квартира Ленина",
          "rooms": 4,
          "address": {
            "city": "Tyumen",
            "street": "Ленина",
            "house": "134",
            "room": "24"
          },
          "area": 134,
          "unit": "квм"
        },
        "relationships": {
          "type": "agent",
          "id": 44,
          "attributes": {
            "first_name": "Степан",
            "last_name": "Карачаев",
            "middle_name": "Иванович"
          }
        }
      },
      {
        "type": "flat",
        "id": 3,
        "attributes": {
          "title": "Квартира Ленина",
          "rooms": 4,
          "address": {
            "city": "Tyumen",
            "street": "Ленина",
            "house": "134",
            "room": "24"
          },
          "area": 134,
          "unit": "квм"
        },
        "relationships": {
          "type": "agent",
          "id": 44,
          "attributes": {
            "first_name": "Степан",
            "last_name": "Карачаев",
            "middle_name": "Иванович"
          }
        }
      }
    ]
  }.response
    },
    components:{
        Card
    }
}
</script>



<style scoped>
.main{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 10px;
}

@media screen and (max-width:1200px) {
    .main{
        grid-template-columns: 1fr 1fr ;
    }
}
@media screen and (max-width:839px) {
 .main{
       display: flex;
       flex-direction: column;
       align-items: center;
       justify-content: center;
       gap: 10px;
    }
}

</style>