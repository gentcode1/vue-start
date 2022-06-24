<template>
<div>

<button v-on:click="Increment()">Increment</button>
<button v-on:click="Decrement()">Decrement</button>
<p>{{count}}</p>
<div class='form'>
    <h1> Get Input Field Value</h1>
    <br/><br/>
    <input type='text' placeholder="enter email" v-model="email"/>
    <br/>
    <input type='text'  placeholder="enter password" v-model="password"/>
    <br/>  
    <button type='password' @click="SubmitData"> Submit</button>
</div><br/><br/>
<div class='form'>
    <h1> Get Check , Radio and Select</h1>
    <label for='React'>React Js</label>
    <input type='checkbox' value='React' v-model="technology"/>
    <label for='View'>View Js</label>
    <input type='checkbox'  value='View' v-model="technology"/>
    <label for='angular'>Angular</label>
    <input type='radio'  value='angular' v-model="profession" name='framework'/>
      <label for='redux'>Redux</label>
    <input type='radio'  value='redux' v-model="profession"  name='framework'/>
    <br/>  
    <h2 >{{technology}}</h2>
    <h2 >this was {{profession}}</h2>
</div><br/><br/>
<div class='form'>
    <h1> If Else Statement</h1>
    <h2 v-if='show'>if condition</h2>
    <h2 v-else>else condition</h2>
    <button @click="show=!show">Check</button>
</div>
<br/><br/>
<div class='form'>
  <ul>
      <li v-for='item in language' :key='item'>{{item}}</li>
      </ul> 
</div>   
<br/><br/>
<div class='form'>
  <ul>
      <li v-for='item in users' :key='item'>email is:{{item.name}} and age is: {{item.age}}</li>
      </ul> 
</div>       
</div>

</template>  
<script>
export default {
    name: "Home",
    data(){
    return {
        count:0,
        email: null,
        password: null,
        technology:[],
        profession: null,
        show:true,
        language:[
           ' Js',
            'Java',
          '  C',
           ' Python',
           ' C++'
        ],
        users:[
            {name:'gent',
            age:'13'},
            {name:'miggi',
            age:'14'},
            {name:'Arth',
            age:'3'},
        ]
    } },
   methods: {
    Increment(){
        
        
        this.count = this.count-1 

        },
       
    
    Decrement(){
              this.count = this.count+1
                
            },
      SubmitData(){
            console.log( "values :" + this.email  +' '+ this.password)
      }      
   }
        
    }

    



</script> 
<style scoped>
h1{
    background: gray
}
.form{
    display:  flex;
    flex-direction: column;
    max-width: 100vw;
    justify-content: center;
    align-items: center;
    
}
</style>
