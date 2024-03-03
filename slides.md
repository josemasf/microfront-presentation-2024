---
theme: ./
layout: intro
transition: slide-left
---

# Introducción a Microfront

Introducción, troceo y técnicas

<template v-slot:icon>
  <div class="grid grid-col-2 w-full h-full">
    <logos-vue class="w-full h-full" />    
    <logos-astro class="w-full h-full" />  
    <logos-react class="w-full h-full" />  
    <logos-angular class="w-full h-full" />  
    <logos-solidjs class="w-full h-full" />      
  </div>  
</template>

---
layout: order-paper
---

<div class="grid grid-cols-4 gap-4 text-white mt-10">
  <OrderPaperItem icon="play" title="El monolito" body="Cuándo se rompie el monolito"/>
  <OrderPaperItem icon="chartPie" title="Troceo" body="Cómo romper el molonito"/>
  <OrderPaperItem icon="crane" title="Técnicas" body="Técnicas montar esta arquitectura"/>
  <OrderPaperItem icon="island" title="Íslas" body="Astro Island"/>                    
</div>

---

# MICROSERVICIOS


La arquitectura de microservicios [...] consiste en construir una aplicación como un conjunto de pequeños servicios, los cuales se ejecutan en su propio proceso y se comunican con mecanismos ligeros (normalmente una API de recursos HTTP) 

https://es.wikipedia.org/wiki/Arquitectura_de_microservicio


---

<img src="/assets/microservice.png" class="object-cover h-full m-auto" />

---

## Ventajas

|     |     |
| --- | --- |
| <b>Modularidad</b> | Se pueden desarrollar y desplegar de forma independiente. |
| <b>Escalabilidad</b>   | Se puede escalar cada parte según sea necesario. |
| <b>Versatilidad</b> | Usar diferentes tecnologías y lenguajes. |
| <b>Rapidez de actuación</b> | Desarrollo menos costoso. |
| <b>Mantenibilidad</b> | Mejoras independientes. |
| <b>Agilidad</b> | Reusar código de terceros. |



---
layout: quote
---

# MICROFRONTEND

Surge en el 2016 por primera vez

> “ Microfrontends es la representacin técnica de un subdominio de negocio, que permite la implementaciones independientes con la igual o distinta tecnología. Por último, se debe evitar compartir logica con otros subdominios y son propiedad de un único equipo”

Luca Mezzalira Vicepresidente de arquitectura en DAZN



---

# Frontends monolíticos


<img src="/assets/monolith-frontback-microservices.png" class="object-cover  m-auto" />


---

## Los problemas del monolito

|     |     |
| --- | --- |
| <b>Mantenimiento </b> | Código desarrollado por muchos de distintos niveles y a lo largo del tiempo, se vuelve complejo. |
| <b>Conflictos de código</b>   | desarrollos en paralelo sobre un mismo repositorio. Los merges de la muerte |
| <b>Una sola tecnología </b> | el monolito implica amplicar una única tecnología en todo la aplicación. |
| <b>Mantenibilidad</b> | las funcionalidades deben estar completas. |


---

# Organización vertical Microfrontend

<img src="/assets/verticals-headline.png" class="object-cover h-80  m-auto" />

---

# ¿Cuándo es recomendable usar esta metodología?

- Grandes aplicaciones
- Múltiples equipos
- Tiempos de entrega distintos

---

## Beneficios

- Al ser más pequeña, la aplicación carga más rápido
- Merge más simples
- Reducción de conflictos entre Merge de otros equipos
- Múltiples framework, según el problema. Transparente al cliente

---

## ¿Cuándo no usar esta metodología?

- Pequeños equipos
- Cuando los microfrontends compliquen el desarrollo
- Cuando no estemos usando métodos automáticos de despliegue
- Cuando el equipo sea demasiado junior.

---

# Cómo trocear la aplicación

|     |     |
| --- | --- |
| <b>Página </b> | Si tiene un buen enrutamiento, puede ejecutar microaplicaciones específicas separadas para cada página. |
| <b>Funcionalidad</b>   | Aislar funcionalidades en una página |


---
layout: iframe
url: https://micro-frontends-es.org/0-model-store/
class: my-cool-content-on-the-left
---


---

<img src="/assets/three-teams.png" class="object-cover h-100  m-auto" />

---
layout: center
class: "text-center"
---

# Técnicas

<div class="flex justify-center items-center ">
  <OrderPaperItem icon="crane" title="Técnicas" body="Técnicas montar esta arquitectura" class="text-dark bg-gray-400 rounded max-w-100 p-10 border-t border-t-red border-t-2"/>
</div>

---
layout: two-thirds
---

## Build-time integration

<template v-slot:first-col>

```js
{
	"name": "@feed-me/container",
	"version": "1.0.0",
	"description": "A food delivery web app",
	"dependencies": {
		"@feed-me/browse-restaurants": "^1.2.3",
		"@feed-me/order-food": "^4.5.6",
		"@feed-me/user-profile": "^7.8.9"
	}
}
```

</template>

<template v-slot:second-col>
  
  ### ¿Quién lo usa?

  <img src="/assets/goalsystems.webp" />
  <img src="/assets/dazn.png" class="max-h-20"/>
</template>


---
layout: two-thirds
---

## Run-time integration via iframes

<template v-slot:first-col>

```html
<iframe id="micro-frontend-container"></iframe>

<script type="text/javascript">
	const microFrontendsByRoute = {
	'/': 'https://browse.example.com/index.html',
	'/order-food': 'https://order.example.com/index.html',
	'/user-profile': 'https://profile.example.com/index.html',
	};

	const iframe = document.getElementById('micro-frontend-container');
	iframe.src = microFrontendsByRoute[window.location.pathname];
</script>
```

</template>

<template v-slot:second-col>
  
  ### ¿Quién lo ha usado?  
  <img src="/assets/spotify.png" />
</template>


---
layout: two-thirds
---

## Web components

<template v-slot:first-col>

Similar a iframe, pero en vez de frames cada front se transforma en un web component
<logos-webcomponents class="w-24 h-24" />    
</template>

<template v-slot:second-col>
  
  ### ¿Quién lo ha usado?  
  <img src="/assets/opentable-logo.svg" class="bg-white" />
</template>

---
layout: two-thirds
---

## Template composition

<template v-slot:first-col>

Se utiliza una página como plantilla, que contiene secciones donde cargaran cada uno de los frontales. Puede hacerse en servidor o cliente.
<img src="/assets/template-composition.png" />

</template>

<template v-slot:second-col>
  
  ### ¿Quién lo ha usado?  
  <div class="flex w-full gap-8">
    <div> 
    Server
    <img src="/assets/paypal-logo.webp" class="bg-white max-h-20" />  
    </div>
    <div>
    Client
    <img src="/assets/iberostar.jpg" class="bg-white  max-h-20" />
    </div>
  </div>

</template>

---
layout: two-thirds
---

## Edge Side Includes

<template v-slot:first-col>

HTML extendido que permite a nodos extremos renderizar ESI (Edge Side Includes), facilita el cacheo pero está en desuso.
<img src="/assets/ikea-code.png" class="max-h-70" />  


</template>

<template v-slot:second-col>
  
  ### ¿Quién lo ha usado?  
  <img src="/assets/ikea.svg" class="" />  

</template>
---
layout: center
class: "text-center"
---
# Meta framework



<div class="flex justify-center items-center ">
  <OrderPaperItem icon="framework" title="Meta framework" body="Heramientas para construir microfrontend" class="text-dark bg-gray-400 rounded max-w-100 p-10 border-t border-t-red border-t-2"/>


</div>


---
layout: iframe-right

# the web page source
url: https://bit.dev/

---

## BIT

Muy común y con muchas recomendaciones, es de pago.


---

## Module Federation

La Federación de Módulos es una característica de Webpack que permite a una aplicación JavaScript cargar de manera dinámica código de otra aplicación en tiempo de ejecución. Esto significa que puedes tener múltiples aplicaciones independientes que comparten código entre sí, pero cada una de ellas puede ser desarrollada y desplegada de manera independiente.

Permite compartir dependencias core entre aplicaciones.

```js
//vite.config
export default defineConfig({
  plugins: [
    vue(),
    federation({
        name: 'host-app',
        remotes: {
            remote_app: "http://localhost:4173/assets/dt-vue2.js",
        },
        shared: ['vue']
    })
  ], ...
})
```

---

## Single SPA

Se crea un orquestador que controla el resto de Frontends y mediente un builder se generan los modulos y se unen.

```js
registerApplication({
  name: "@vue-mf/dogs-dashboard",
  app: () => System.import("@vue-mf/dogs-dashboard"),
  activeWhen: "/view-doggos",
});
```

```js
{
  "imports": {
    "@react-mf/navbar": "https://localhost:8080/react-mf-navbar.js",
    "@react-mf/planets": "https://react.microfrontends.app/planets/~/react-mf-planets.js",
    "@react-mf/things": "https://react.microfrontends.app/things/~/react-mf-things.js"
    "@vue-mf/dogs-dashboard": "https://react.microfrontends.app/things/~/vue-mf-dogs-dashboard.js"
  }
}
```

---

## Otros

- Podium
- Systemjs
- Piral
- Open Components
- Qiankun -> basado en single-spa.
- Luigi
- FrintJS



---
layout: center
class: "text-center"
---

# Íslas

<div class="flex justify-center items-center ">
  <OrderPaperItem icon="island" title="Íslas" body="Astro Island" class="text-dark bg-gray-400 rounded max-w-100 p-10 border-t border-t-red border-t-2"/>
</div>

---
layout: image-right

# the image source
image: /assets/islands-architecture.png
backgroundSize: 100% 90%
---

## Islands Architecture

En la arquitectura de Islas, una página web se compone de "islas" de componentes interactivos que se cargan de forma diferida. Esto significa que el HTML y CSS se cargan primero, y luego los componentes interactivos (generalmente escritos en JavaScript) se cargan y se hidratan solo cuando son necesarios.

[Islands Architecture - Katie Sylor-Miller](https://jasonformat.com/islands-architecture/)


---

## Puntos fuertes de las íslas

Aunque la mayoría de los desarrolladores se quedarán con un solo framework de UI, Astro admite múltiples frameworks en el mismo proyecto. Esto te permite:

- Escoger el framework que sea mejor para cada componente.
- Aprender un nuevo framework sin necesidad de iniciar un nuevo proyecto.
- Colaborar con otros incluso cuando trabajan en diferentes frameworks.
- Convertir gradualmente un sitio existente a otro framework sin tiempo de inactividad.


---

## Conclusión

### Las íslas nos permiten tener un monolíto rompiendo la condición de una sólo framework/libreria en el front

En Astro, depende de ti como desarrollador decirle explícitamente a Astro cuáles componentes de la página deben ejecutarse también en el navegador. Astro solo hidratará exactamente lo que se necesita en la página y dejará el resto de tu sitio como HTML estático.

<logos-astro class="w-full h-40 p-10" />

---
layout: center
class: "text-center"
---

# Gracias
<div class="flex justify-center items-center gap-10">
  <div>
    <logos-linkedin-icon /> AIDA Canarias
  </div>
  <div>
    <logos-twitter /> @AIDASoftwate
  </div>
  <div>
    <logos-chrome /> aidacanarias.com
  </div>  
</div>

<Confetti class="top-50 relative" />
