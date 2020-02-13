# PeopleSpace
## Basic for arrainging web page layout 
<img width="500" alt="screen" src="https://user-images.githubusercontent.com/55173544/74410245-87d9b080-4ded-11ea-9197-a86c5b79eb85.png">
<br><br><br>  

1. Flex  
+ Flex must be a **parent** and **child** structure.  
+ The first step of flex is to give `display: flex` style on the **parent** tag.  

<.html>  
 ``` 
    <div class="container_y">       /*parent1*/
      <div class="row">             /*child1*/
        <div class="container_x">               /*parent2*/
          <div class="item">1</div>             /*child2*/
          <div class="item">2</div>  
          <div class="item">3</div>  
        </div>  
       </div>  
      
      <div class="row">            
        <div class="container_x">            
          <div class="item">4</div>           
          <div class="item">5</div>  
          <div class="item">6</div>  
        </div>  
       </div>   
      
    </div>  
 ```  
<.css>  
```  
.container_y{  
  background-color: powderblue;  
  display: flex; 
  flex-direction: column;
} 
.row{
  background-color: yellow;
  border:1px solid white;
  width: 50px;
  height: 60px;
}
.container_x{  
  background-color: grey;  
  display: flex; 
  width:800px;
} 
.col{
  background-color: tomato;
  border:1px solid white;
  width: 50px;
  height: 60px;
}
```  
<img width="856" alt="스크린샷 2020-02-13 오전 12 33 07" src="https://user-images.githubusercontent.com/55173544/74415607-8feb1d80-4df8-11ea-8fb2-60f85ff83121.png">  

+ You can give one `col` a specific width.  

<.css>  
```  
*  
*  
*  
.col:nth-child(2){
  flex-basis: 100px;
}  
```  

<img width="856" alt="스크린샷 2020-02-13 오전 12 33 19" src="https://user-images.githubusercontent.com/55173544/74415681-ab562880-4df8-11ea-8321-411b69592e19.png">  

+ You can use `flex-grow` to fill the blanks.

<.css>  
```  
*  
*  
*  
.col:{
  flex-grow:1;
}  
```  

<img width="856" alt="스크린샷 2020-02-13 오전 12 33 34" src="https://user-images.githubusercontent.com/55173544/74415840-f839ff00-4df8-11ea-8045-97337c4b5ee0.png">
