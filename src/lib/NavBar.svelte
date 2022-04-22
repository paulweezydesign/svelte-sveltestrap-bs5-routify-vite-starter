<script>

	import Icon from '/src/assets/Icon.png';
 
  import { Button, Offcanvas } from 'sveltestrap';
  
  let open = false;
  const toggle = () => (open = !open);
</script>



<nav class="bg-primary text-light">
    <div class="NavBrand">
      <h1 class="fw-bold">Svelte</h1>
    </div>
    <div class=" ">
      <div class="d-md-none d-flex justify-content-end Side">
       <Button class="fs-1" color="primary" on:click={toggle}><img src={Icon} alt="menu icon"></Button>
       <Offcanvas class=" OffCanvas " isOpen={open} {toggle}  placement="start">
         <h1 class="text-center" slot="header">
            <b>menu</b>
         </h1>
         <div class="NavLinks text-center d-flex flex-column  fs-2">
           <a class="nav-link " href="/">Home</a>
           <a class="nav-link  " href="/about">About</a>
           <a class="nav-link " href="/contact">Contact</a>
           <a class="nav-link " href="/blog">Blog</a>
         </div>
       </Offcanvas>
      </div>
     
     <div class="NavLinks text-light d-none d-md-flex fs-2">
       <a class="nav-link text-light" href="/">Home</a>
       <a class="nav-link text-light " href="/about">About</a>
       <a class="nav-link text-light" href="/contact">Contact</a>
       <a class="nav-link text-light" href="/blog">Blog</a>
     </div>
    </div>
   
   
   </nav>


   <style>
nav {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr;
    align-items: center;
    height: 100px;
    width: 100vw;
    
  }
.NavBrand {
  margin-left: 12%;
}
 .NavLinks {
   display: flex;
   justify-content: end;
   margin-right: 12%;
 }
 .Side {
   margin-right: 12%;
 }
 .OffCanvas {
   height: 100px;
 }
       
   </style>