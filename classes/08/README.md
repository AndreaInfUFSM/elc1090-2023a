<!--
author:   Andrea Charão

email:    andrea@inf.ufsm.br

version:  0.0.1

language: PT-BR

narrator: Brazilian Portuguese Female

comment:  Material de apoio para a disciplina
          ELC1090 - Desenvolvimento de Software para Web
          da Universidade Federal de Santa Maria

translation: English  translations/English.md
-->

<!--
liascript-devserver --input README.md --port 3001 --live
https://liascript.github.io/course/?https://raw.githubusercontent.com/AndreaInfUFSM/elc1090-2023a/master/classes/08/README.md
-->


# Segundo projeto



> Objetivo: Criar aplicação web com propósito e funcionalidades à sua escolha, consumindo API pública (sem autenticação) também à sua escolha

## Criatividade à mostra

> Neste projeto não teremos clientes entre os colegas, mas... No final vamos compartilhar as criações com os demais colegas de curso!

## Parcerias

> Este projeto é individual, mas cada estudante deverá indicar um(a) colega parceiro de testes/mentoria.


## Que API?!

- No material da aula anterior há links para listas de APIs, que podem ser usadas isoladamente ou em combinadas

- Você também pode criar sua API, que deve ter pelo menos um endpoint público mas também pode ter outros privados

## Como desenvolver?

- Você pode escolher entre:

  1. usar os recursos exercitados na última aula (HTML, CSS/Bootstrap e JavaScript) ou 
  2. escolher algum framework que você já conheça ou deseje conhecer

- Proibido: desenvolver todo o trabalho em plataformas no-code 


# Projetos

- Cada estudante vai preencher sua proposta no formulário da página seguinte
- A proposta será validada pela professora

## Preencha sua proposta

> Clique abaixo para criar seu repositório de entrega:

https://classroom.github.com/a/xSdStO2_

> Preencha este formulário para adicionar sua proposta na lista:

<form id="formproject2">
      <label for="developer">Seu nome:</label><br>
      <input class="lia-input lia-quiz__input" name="developer" type="text" required> <br>
      <label for="client">Parceria(s):</label><br>
      <input class="lia-input lia-quiz__input" name="partner" type="text" placeholder="Nome de colega(s)..." required> <br>
      <label for="project">Descrição do projeto:</label><br>
      <input class="lia-input lia-quiz__input" name="project" type="text" placeholder="Descreva brevemente seu projeto" required> <br>
      <label for="api">API(s):</label><br>
      <input class="lia-input lia-quiz__input" name="api" type="text" placeholder="API(s) web que você vai usar" required> <br>
      <label for="tech">Tecnologias:</label><br>
      <input class="lia-input lia-quiz__input" name="tech" type="text" placeholder="Por exemplo: HTML, CSS, Bootstrap, frameworks, etc." required> <br>
      <label for="github">Repositório de entrega no GitHub:</label><br>
      <input class="lia-input lia-quiz__input" name="github" type="text" placeholder="Crie seu repositório antes de preencher" required> <br>
      <label for="deploy">Plataforma de hospedagem escolhida:</label><br>
      <input class="lia-input lia-quiz__input" name="deploy" type="text"  placeholder="Indique a que você pretende usar" required> <br>

      <button class="lia-btn lia-btn--outline" type="submit">Submit</button>
   </form>
   <script>
      (function () {
         formproject2.addEventListener('submit', function (e) {
            // Prevent default behavior
            e.preventDefault();
            // Create new FormData object
            const formData = new FormData(formproject2);
            // Convert formData object to URL-encoded string
            const payload = new URLSearchParams(formData);            
            //send.lia("Adicionando...", false)
            alert("Sua proposta será adicionada!")
            //document.getElementById("loader").innerText = "xx"; //style.display = "block";
            const event = new MouseEvent("click", {
              view: window,     
              bubbles: false,
              cancelable: false});
            const elem = document.getElementById("lia-btn-next");
            elem.dispatchEvent(event);
            // Post the payload using Fetch
            fetch("https://script.google.com/macros/s/AKfycbzVnYewBduUclZlt6uchNsxQI-kOhGvX8QGvoQQCf9tfWtdNxgRQkX9YquXjMszf763LQ/exec?action=postProject2&" + payload)
            //.then((response) => response.json())
            //.then((json) => {send.lia("LIA: clear"); alert("Projeto adicionado!")} )            
            //.then((json) => {send.lia(json.message, false); alert("Projeto adicionado!")} )
            //.then((json) => send.lia(json.message, false)) 
         })
      })()
   </script>


## Em andamento


> Lista de projetos em andamento (seja paciente, a carga pode demorar alguns segundos)

 <script>
    let mylist = ''
    fetch('https://script.google.com/macros/s/AKfycbzVnYewBduUclZlt6uchNsxQI-kOhGvX8QGvoQQCf9tfWtdNxgRQkX9YquXjMszf763LQ/exec?action=getProjects2')
      .then(response => response.json())
      .then(data => data.objects.forEach(project => { 
        mylist += "- " + "**Developer: " + `${project.developer}` + "**\n\n" + 
                  "  " + "Parceria: " + `${project.partner}` + "\n\n" + 
                  "  " + "Projeto: " + `${project.project}` + "\n\n" +
                  "  " + "API(s): " + `${project.api}` + "\n\n" +
                  "  " + "Tecnologias: " + `${project.tech}` + "\n\n" +
                  "  " + "Repositório: " + `${project.github}` + "\n\n" +
                  "  " + "Hospedagem: " + `${project.deploy}` + "\n\n" +
                  "  " + "Status: " + `${project.status}` + "\n\n" 
        send.liascript(mylist) // this shouldn't be here
        }))        
    
    "Loading..."
</script>

## Entrega


- Caso ainda não tenha criado seu repositório de entrega, clique aqui para fazer isso: https://classroom.github.com/a/xSdStO2_
- Você vai preencher um README.md semelhante ao das atividades anteriores (acompanhe as aulas para obter o modelo)

## Apresentação

Aguarde orientações