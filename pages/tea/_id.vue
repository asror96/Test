<template>
  <section>
  <h1 style="text-align: center">
    {{items[$route.params.id].title}}
  </h1>
  <div>
    <img style="height: 150px; width: 100px;display: block;margin-left: auto;margin-right: auto;" :src="items[$route.params.id].img" alt="Card image cap"/>
  </div>
    <i>{{items[[$route.params.id]].description}}</i>
    <p class="card-text"><small class="text-muted">{{now.getDate()}}.{{now.getMonth()}}.{{now.getFullYear()}}</small></p>
    <h5>Comment(after enter the text press enter): <br>{{comment}}</h5>
    <textarea type="text" v-on:keyup="commentation"></textarea>
  </section>
</template>
<script>
export default {
  data: ()=>({
    items:
      [{
        id:1,
        title:'Tess Pleasure',
        img:'https://ir-2.ozone.ru/s3/multimedia-r/wc700/6028472499.jpg',
        description:'Крупнолистовой байховый чай, дополненный ароматным шиповником, сладким яблоком, бодрящим лимонным сорго и нежными лепестками незабудки и василька. При заваривании имеет насыщенный цвет и глубокий аромат с карамельными нотками. Добавки не перебивают вкус чая и дают ему полностью раскрыться, несмотря на ароматизатор в составе. Отличное сочетание вкуса, качества и цены.'
      },{
        id:2,
        title: 'Tisun из 6 баночек',
        img:'https://ir-2.ozone.ru/s3/multimedia-u/wc700/6702176802.jpg',
        description:'Крупнолистовой байховый чай, дополненный ароматным шиповником, сладким яблоком, бодрящим лимонным сорго и нежными лепестками незабудки и василька. При заваривании имеет насыщенный цвет и глубокий аромат с карамельными нотками. Добавки не перебивают вкус чая и дают ему полностью раскрыться, несмотря на ароматизатор в составе. Отличное сочетание вкуса, качества и цены.'
      },{
        id:3,
        title:'Принцесса Нури',
        img:'https://ir-2.ozone.ru/s3/multimedia-h/wc700/6035663345.jpg',
        description:'Авторский купажированный набор чаёв серии DeTox включает в себя 6 видов чая: зелёный с имбирём и мёдом, малину с мятой, чёрный с чабрецом, успокаивающий из мелиссы, лаванды и гибискуса, зелёный с жасмином, микс здоровья из садовых трав. Каждый вид чая упакован в стеклянную баночку, а сам набор — в крафтовую коробку. Идёт в комплекте с подставкой для банок. Tisun DeTox идеально подойдёт в качестве подарка или дегустационного набора для любителей чая.'
      },{
        id:4,
        title:'Каркаде Ceremony' ,
        img:'https://ir-2.ozone.ru/s3/multimedia-6/wc700/6625725054.jpg',
        description:'Классический насыщенный и терпкий купаж чая с высокогорных плантаций Цейлона и Индии. Производится из мелколистового байхового чая. При однократном заваривании получается крепкий напиток с приятным ароматом и лёгким традиционным вкусом. Отлично сочетается с лимоном и мятой. Экономичная упаковка на 100 пакетиков. Не содержит искусственных красителей и консервантов.'
      },{
        id:5,
        title:'Бабушкино Лукошко',
        img:'https://ir-2.ozone.ru/s3/multimedia-d/wc700/6131969749.jpg',
        description: 'Глубокий вишнёвый цвет и выразительный ягодный вкус с кислинкой — этот чай каркаде хорош как в горячем, так и в охлаждённом виде. Чай содержит антиоксиданты, множество витаминов и микроэлементов. Способствует укреплению иммунитета и похудению. В чае Ceremony не содержится ничего, кроме высушенных лепестков суданской розы, которые не подвергались ферментации. Натуральный состав и сбалансированный вкус — визитная карточка этого каркаде.'
      }],
    now: new Date(),
    comment:''
  }),
  methods:{
    commentation: function (event){
      if(event.keyCode===13){
        this.comment=event.target.value
      }

    }
  }
}
</script>
