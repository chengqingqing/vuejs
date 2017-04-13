# vuejs
vue 生命周期简单描述

var myVue = new Vue({
                
        });
        
        生命周期可以理解成一个模拟生命的循环
       var vm = new Vue({ }); //创建一个实例化的模型，这个模型的名叫Vm， 可以理解成制造出了一个鲜活的生命体，可以运动，可以被调用，可以到处跑，但是没有任何的意识，也没有数据
       var vm =  new Vue({ el:'#app', data: { name: 'liming' } }) /／这里定义一个name 的属性， 这这里它开始有自己的个性了 在页面中，el 规定了它只能在某个活动区域内跑，
       var vm =  new Vue({ 
          el:'#app',
          data:{name:'liming'},
          
          这个Vm 在实例化之后 就是刚生下来 
          beforeCreate: function(){}  
          
          这里已经完成了  数据观测  属性和方法 的运算  事件回调 
          created: function(){} 
          
          挂载之前使用 挂载就是 $el 属性不能用
          beforeMount: function(){} 
          
          挂载到实例上了，原有的 el 被新创建的  vm.$el 替换了 
          mounted: function(){} 
          
          当数据更新时调用 
          beforeUpdate: function(){}  
          
          由于数据的修改，虚拟DOM 重新渲染和打补丁 这个之后调用该钩子
          updated: function(){} 
          
          <keep-alive></keep-alive> 组件被激活的时候可以调用   不用这个组件的时候这个用不上
          activated : function(){}
          
          <keep-alive></keep-alive> 组件被停用的时候可以调用
          deactivated : function(){}
          
          
          实例被销毁之前调用 这一步实例仍然可以使用
          beforeDestroy : function(){}
          
          实例被销毁后调用，调用之后 实例指示的所有东西都会解除绑定
          destroyed : function(){}
          
          
          
          
          })
        
        
        
        
        
        
        
