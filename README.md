# hello_vue3
# vue3 的初步学习
  ##  区别于 vue2  选项式optionapi 
            组成式componentapi  


            不能在setup函数中用this
            setup函数中写数据 和方法
            在setup外同样能够写vue2中的data  computed  watch 等
            但是不能在vue2中使用  组件里的  data  computed  watch 等
            组件里的东西  必须写在setup中
            setup中必须要写 return  并且return出去的东西  必须要在template中使用
            setup函数中可以调用vue2中的方法
            在data中能用this读到setup函数中的数据
            重新写一个script标签去替代setup函数
            <script lang="ts" setup>
            
            </script>
            相当于一个setup函数
            

##   vue3中两个
            ref  响应式数据  基本类型数据  也能定义对象类型的响应式数据
            reactive  响应式对象  只能定义对象类型的数据
            区别
            ref  响应式数据  必须要写.value  才能读取到数据
            reactive  响应式对象  可以直接读取到数据
            但是ref  响应式数据  不能是对象  因为ref  响应式数据  是通过Object.defineProperty()来实现的
            而Object.defineProperty()不能监听对象的属性  只能监听属性的变化
            所以ref  响应式数据  不能是对象  但是reactive  响应式对象  可以是对象
            因为reactive  响应式对象  是通过ES6的Proxy来实现的  可以监听对象的属性的变化

            想让哪里数据是响应式的，就把这个数据用ref包起来

            第一件在script标签里引入reactive
            将对象用reactive包起来


 ### v-for循环
            用v-for循环出来的东西  必须要写在template中
            用v-for循环出来的东西  必须要写在template中
            用v-for循环出来的东西  必须要写在template中
            <v-for="(item,index) in list" :key="index">
                {{item}}
            </v-for>
## 用ref定义对象类型的响应式数据
            用ref定义对象类型的响应式数据  必须要写.value  才能读取到数据
            用ref定义对象类型的响应式数据  必须要写.value  才能读取到数据
            用ref定义对象类型的响应式数据  必须要写.value  才能读取到数据
