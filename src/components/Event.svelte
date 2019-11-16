<script>
  export let name;
  export let date;
  export let timing;
  export let venue;
  export let custclass;
</script>

<style lang="scss">
.box-wrap{display: flex; justify-content: space-around;}
  .box{
    background: #201c29;
    color: #a1a1af;
    -webkit-box-shadow: 0 0 2rem #000;
    box-shadow: 0 0 2rem #000;
    width:100%;
    margin:0 10px;
    width: 90%;
    margin: 25px 10px;
    padding: 10px 20px;
   
  }
   .purple{
          background: #311e5e; 
    }
    .red{
          background: #d12121;
    }
    .green{
          background: #0d4319;
    }
  span{
    margin:0 20px 10px 0;
    padding-bottom: 10px;
  }
  h1{
    padding: 10px 0;
    margin: 5px 0;
    color: #ffc;
  }
  .mb-20{
    margin-bottom:20px;
  }
  .venue{ display: flex;
    justify-content: flex-end;}
</style>
<div class="box-wrap">
<div class="box {custclass}">
  <h1>{name}</h1>
  <div class="mb-20 " style="justify-content:space-around;"><span>Date: {date}</span> <span>Timing: {timing}</span>
  <div class="mb-20 venue">Venue: {venue}</div>
  </div>
  
</div>
</div> 

