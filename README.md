# task_tyumen

1) Не сработает первый фрагмент кода, тк есть такое понятие, как поднятие переменной (hoisting), наш первый фрагмент выглядит так:
т.е. объявление переменной будет всегда в верху скрипта, и когда мы захотим вывести пустую переменную, в которой ничего нет, у нас будет doubleNum не определён

let doubleNum;                       
console.log( doubleNum(10) );  //doubleNum is not defined

	doubleNum = (num) => {
		let result = num * 2;
		return result;
	}

-----------------------------------------

2) <template>
  <component-name
      v-for="i in filteredCount"
      :key="i"
  />
</template>
<script>
export default {
  data() {
    return {
      count: 20
    };
  },
  computed: {
    filteredCount() {
      return this.count < 10 ? this.count : 9
    }
  }
}
</script>
---------------------------------

3) resources = [
			{
			   id: 1,
			   count: 13,
   			},
			{
			   id: 2,
			   count: 5,
   			}, 
			{
			   id: 3,
			   count: 24,
   			},
		      {
			   id: 4,
			   count: 101,
   			}, 
			{
			   id: 5,
			   count: 72,
   			}, 
			{
			   id: 6,
			   count: 64,
   			}, 
			{
			   id: 7,
			   count: 305,
   			}, 
			{
			   id: 8,
			   count: 67,
   			}, 
			{
			   id: 9,
			   count: 95,
   			}, 
			{
			   id: 10,
			   count: 21,
   			}, 
			{
			   id: 11,
			   count: 37,
   			},
		   ];


		   function resourceTask(resources){
		       let obj = {};

           for (let n = 0; n < resources.length; n++) {
              obj[resources[n]['id']] = resources[n]['count'];
           }

            return obj;
		   }
		   
	       console.log(  resourceTask(resources) );


