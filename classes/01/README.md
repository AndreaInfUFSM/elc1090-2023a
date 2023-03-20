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
https://liascript.github.io/course/?https://raw.githubusercontent.com/AndreaInfUFSM/elc1090-2023a/master/classes/01/README.md
-->

# Dinâmica: “not no-one, not everyone”



## Indique

Indique a URL de um site que você conhece e acredita que alguém mais da turma conheça, mas não toda a turma.



    [[___]]
<script>
  let input = encodeURIComponent(`@input`.trim())
  send.lia("Adicionando...", [], false)
  fetch("https://script.google.com/macros/s/AKfycbzVnYewBduUclZlt6uchNsxQI-kOhGvX8QGvoQQCf9tfWtdNxgRQkX9YquXjMszf763LQ/exec?action=postSite&url=" + input)
  .then((response) => response.json())
  .then((json) => send.lia(json.message, [], false));

</script>



## Visualize




 <script>
    let mylist = ''
    fetch('https://script.google.com/macros/s/AKfycbzVnYewBduUclZlt6uchNsxQI-kOhGvX8QGvoQQCf9tfWtdNxgRQkX9YquXjMszf763LQ/exec?action=getSites')
      .then(response => response.json())
      .then(data => data.objects.forEach(note => { 
        mylist += "- " + `${note.url}` + "\n"
        send.liascript(mylist) // this shouldn't be here
        }))        
    
    "Loading..."
</script>


## Conheça (dynamic)



 <script>
    let mylist = ''
    fetch('https://script.google.com/macros/s/AKfycbzVnYewBduUclZlt6uchNsxQI-kOhGvX8QGvoQQCf9tfWtdNxgRQkX9YquXjMszf763LQ/exec?action=getSites')
      .then(response => response.json())
      .then(data => data.objects.forEach(note => { 
        mylist += "Conhece  " + `${note.url}` + "?\n\n    [(sim)] Sim\n    [(nao)] Não\n\n"
        send.liascript(mylist,[],false) // this shouldn't be here
        }))        
    
    "Loading..."
</script>








## Conheça (static)




1. Conhece http://www.ufsm.br ?

    [(sim)] Sim
    [(nao)] Não




2. Conhece http://www.ufsm.br ?

    [(sim)] Sim
    [(nao)] Não





