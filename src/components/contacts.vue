<template>
<div class="contacts">
    <div class="container" >
        <div class="row mx-auto text-center">
            <h1><span class="h1">π²</span>πΎπ½ππ°π²ππ</h1>
        </div>
        <div class="row">
            <div class="col mx-auto text-center" id="col">
                <h4>
                    <span class="h4">πΏ</span>ππππππ πππ πΎππππ πππππππ   
                </h4>
                <p>
                    <span id="first">πΏ</span>ππππ: +πΈπ½ πΎπ· πΈπΌπΈ πΊπΈπ»πΊ
                </p>
                <p>
                    <span id="first">π΄</span>ππππ: ππππ@π-πππππ.ππ.π£π
                </p>
                <h6 class="mx-auto text-center">
                    <span class="h6">π΅</span>πππ πππ ππππ π·πΆ:πΆπΆπ°πΌ πππ π·πΏ:πΆπΆπΏπΌ πππ ππππππππ ππππππππ ππππ ππ π ππππππ πππππ ππππ ππ πππππ’ πππ ππππ π’ππ π πππ π’πππ ππππππππ. π±πππ πππ π·πΈ:πΉπΆπΏπΌ πππ π·πΉ:πΈπΆπΏπΌ πππ ππππππππ πππππππ ππππ π πππ ππ ππ πππππ ππ πππππ π πππ ππ π ππππππ πππππ’ ππ π’πππ πππππππππ.
                </h6>
                <h5>
                    <span class="h5">π</span>πππππ/ππππππ πΈπππ
                </h5>
                <p>
                    <span id="first">π</span>πππππ@π-πππππ.ππ.π£π
                </p>
                <button>
                    ππππππ ππππππ/ππππππ πππππππ 
                </button>
                <h5>
                    <span class="h5">π²</span>πππππ πΏππππππ π΄ππππππππ
                </h5>
                <p>
                    <span id="first">π</span>πππππππ@π-πππππ.ππ.π£π
                </p>
                <h5>
                    <span class="h5">π°</span>ππππππ
                </h5>
                <p>
                    <span id="first">π»</span>π½πΎ π²ππππππππ ππππ | π³ππ π πππ π | πΉππππππ
                </p>
                <p>
                    <span id="first">π</span>π'ππ πΎπππ π΅πππ πΏ:πΆπΆπ°πΌ πππ π·π½:πΆπΆπΏπΌ(πΌπππππ’ ππ π΅πππππ’)
                </p>
                <p>
                    <span id="first">π</span>π'ππ πΎπππ π΅πππ πΏ:πΆπΆπ°πΌ πππ π·π»:πΆπΆπΏπΌ(ππππππππ’)
                </p>
            </div>
            <div class="col p-5">
                <form action="https://formspree.io/f/xnqrjzlo" method="post">
                <h4>
                    <span class="h4">πΌ</span>ππππππ ππ 
                </h4>
                <div>
                    <label>
                        <span class="label">π½</span>πππ πππ π»πππππππ: <span>(Required)</span>
                    </label>
                    <div class="row">
                       <input name="name" placeholder="π΄π: πΉπππ π³ππ">
                    </div>
                    
                </div>
                <div>
                    <label>
                        <span class="label">π΄</span>ππππ: <span>(Required)</span>
                    </label>
                    <div class="row">
                      <input name="email" placeholder="π΄π: ππππ@πππππ.πππ">
                    </div>
                    
                </div>
                <div>
                    <label>
                        <span class="label">πΏ</span>ππππ: <span>(Required)</span>
                    </label>
                    <div class="row">
                        <input name="phone" placeholder="π΄π: +πΈπ½ π·πΈ πΉπΊπΌ π½πΎπΏπΆ">
                    </div>
                    
                </div>
                <div>
                    <label>
                        <span class="label">πΌ</span>ππππππ:
                    </label>
                    <div class="row">
                        <input id="message" name="text" placeholder="ππππ ππ π’πππ πππππππ">
                    </div>
                    
                    <button type="submit">
                        ππππ
                    </button>
                </div>
            </form>
            </div>
    </div>
    </div>
</div>
</template>

<style scope>
.contacts{
    padding-top:50px;
    padding-bottom:50px;
    background-color:rgb(243, 243, 243);
}
span{
    color:gray;
    font-family:cursive;
    font-size:13px;
}
h6{
    width:400px;
    font-size:14px;
    font-weight:100;
}
label{
    font-size:20px
}
.row{
    margin-bottom:18px;
}
input{
    margin-left:13px

}
    .h1{
  font-size: 52px;
  color:rgb(210, 14, 70);
  font-weight:bolder;
}
.h2{
  font-size:39px;
  color:rgb(210, 14, 70);
  font-weight:bolder;
}
.h3{
  font-size:40px;
  color:rgb(210, 14, 70);
  font-weight:bolder;
}
.h4{
  font-size:35px;
  color:rgb(210, 14, 70);
  font-weight:bolder;
}
.h5{
  font-size:30px;
  color:rgb(210, 14, 70);
  font-weight:bolder;
}
.h1{
  font-size:50px;
  color:rgb(210, 14, 70);
  font-weight:bolder;
}
#first{
  font-size:27px;
  color:rgb(210, 14, 70);
  font-weight:bolder;
}
.label{
  font-size:20px;
  color:rgb(210, 14, 70);
  font-weight:bolder;
}
p{
    font-weight:200 
}
button{
    border-width:1px;
    height:40px;
    padding:5px;
    border-radius:5px;
    width:300px;
    margin-bottom:10px;
    font-size:13px;
    background-color:rgb(255, 255, 255);
    color:rgb(0, 0, 0);
    font-weight:bold;
}
button:hover{
    background-color:rgb(0, 0, 0);
    color:rgb(255, 255, 255)
}
#message{
    height:200px
}
@media screen and (max-width:576px){
    h6{
        width:300px;
    }
    input{
        width:280px;
        margin-left:0px;
        /* margin-right:5px */
    }
}
@media screen and (max-width:320px){
    button{
        width:280px;
    }
    h6{
        width:260px
    }
}
</style>