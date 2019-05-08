<template>
  <div id="app">
     <!--"toggleable" indica en que tamaño de pantalla colapsara el nav-->
     <b-navbar toggleable="md" type="dark" variant="danger">
        <b-container>
          <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
          <b-navbar-brand href="#">NavBar</b-navbar-brand>
           <b-collapse id="nav-collapse" is-nav>
             <b-navbar-nav>
               <!--":to=" es usado para indicar que elemnto esta activo-->
               <!--No se debe programar nada en script, la redireccion y funcionalidad la realiza solo-->
               <b-nav-item :to="{name: 'home'}" exact>Home</b-nav-item>
               <b-nav-item :to="{name: 'about'}">About</b-nav-item>
               <b-nav-item :to="{name: 'grid'}">Grid</b-nav-item>
               <b-nav-item :to="{name: 'cards'}">Cards</b-nav-item>
               <b-nav-item :to="{name: 'form'}">Form</b-nav-item>
             </b-navbar-nav>
           </b-collapse>
        </b-container>
     </b-navbar>
     <b-container>
       <!--Muesta las vistas de la pagina SPA-->
       <router-view/>
     </b-container>
  </div>
</template>
