---
layout: post
title:  "Experimentando gráficos con Mermaid para Markdown"
author: hernan
categories: [ Skills ]
tags: [ web, mermaid, Google, html5, css ]
image: assets/thumbnails/22-hernan-markdown.png
comments: false
---

Este mundo de la programación funciona muy diferente al resto, acá se comparte códigos y se solucionan bloqueos o problemas de manera conjunta, con quien lo sepa, alguién que de seguro solo conoces por su nick. Por ello, dejo por aquí, este simple código de Mermaid que sirve para hacer gráficos en Markdown.

Lo estoy haciendo usando el trabajo completo de mermaidAPI llamada a través de la CDN según la página de [Mermaid](https://mermaid-js.github.io/mermaid/#/n00b-gettingStarted)

<html>
    <body>
        <script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
        <script>
            mermaid.initialize({ startOnLoad: true });
        </script>
        
        
        Probando...
        <div class="mermaid">
        graph TD    
            A --> B; A --> C; B --> D; C --> D;
        </div>
        
         <div class="mermaid">
        graph TD    
             A --> B
             A --> C
             B --> D
             C --> D;
        </div>
        
        Mermaid con otro diagrama
        <div class="mermaid">
            graph TD 
            A[Client] --> B[Load Balancer] 
            B --> C[Server1] 
            B --> D[Server2]
        </div>
        <br>
        Tercera prueba:
        <div class="mermaid">
            graph TD 
            A[Client] -->|tcp_123| B
            B(Load Balancer) 
            B -->|tcp_456| C[Server1] 
            B -->|tcp_456| D[Server2]
        </div>
    </body>
</html>

  <script src="https://unpkg.com/mermaid@8.9.3/dist/mermaid.min.js"></script>
<script>
  $(document).ready(function () {
    mermaid.initialize({
      startOnLoad:true,
      theme: "default",
    });
    window.mermaid.init(undefined, document.querySelectorAll('.language-mermaid'));
  });
</script>
