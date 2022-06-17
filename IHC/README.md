# Heurísticas de Nielsen e WCAG

## Exemplos de acertos

<details>
   <summary><b>1. Visibilidade do status do sistema</b></summary>
    <br>
    O sistema deve mostrar o que está acontecendo em tempo real pro usuário, um exemplo disso é a interface das playlists Youtube, que ficam ao lado direito do vídeo, mostrando qual vídeo da lista estamos assistindo, qual os próximos e quais já foram assistidos

  <div align="center">
    <img alt="Captura da tela do youtube mostrando a playlist" src="https://user-images.githubusercontent.com/69374340/174390708-81097346-6edd-4465-9ec8-9fa9024b8d17.png">
  </div>
</details>

<details>
   <summary><b>3. Controle e liberdade para o usuário</b></summary>
    <br>
    O sistema deve permitir que o usuário tenha liberdade para realizar ações que ele deseja, mas em caso de acionar alguma ação por engano, deve haver um modo de desfazer (sair de uma janela indesejada ou retornar a um ponto anterior). Um exemplo é a ação de “desfazer” do Google quando a ação é exclusão de um e-mail.

  <div align="center">
    <img alt="Captura da tela do aviso que permite o usuário desfazer a esclusão de um email no Gmail" src="https://user-images.githubusercontent.com/69374340/174390768-69c3d030-04cb-4148-a292-b4146723795d.png">
  </div>
</details>

<details>
   <summary><b>5. Prevenções de erros</b></summary>
    <br>
    Melhor que deixar o usuário resolver um erro é evitar que ele cometa erros, um exemplo disso é a busca do Google, que enquanto estamos digitando na barra de pesquisa ele apresenta algumas sugestões mas também corrigindo erros de ortografia caso tenhamos pesquisado algo errado.

  <div align="center">

|                                                                 Realizando uma busca no Google                                                                 |                                                                                         Resultado da busca com erro de ortográfica                                                                                          |
| :------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| ![Captura de tela da funcionalidade de busca do Google](https://user-images.githubusercontent.com/69374340/174390776-748984f4-284e-45eb-b9ab-763c6857c3f3.png) | ![Captura de tela da funcionalidade de sugestão do Google ao fazer uma pesquisa com termos errados ortograficamente](https://user-images.githubusercontent.com/69374340/174390777-a6f9339e-904c-47c1-a406-b2b48a12b482.png) |

</div>
</details>

---

## Exemplos de erros

<details>
   <summary><b>Exemplo 1</b></summary>
    <br>

  <div align="center">
    <img alt="Captura de tela de site com muitas cores, elementos piscando, rodando, entre outros exageros" src="https://user-images.githubusercontent.com/69374340/174390775-91cc70bf-b092-4775-9cef-5f90b992cc9c.png">
  </div>

> **Observações:** muitas cores misturadas, não colaborando para uma harmonia visual; texto ilegível por conta do baixo contraste entre o background e a cor do texto, além de não utilizar uma fonte simples e de fácil legibilidade; elementos piscando e se mexendo em todos os cantos da tela, podendo representar certo risco de convulsão

</details>

<details>
   <summary><b>Exemplo 2</b></summary>
    <br>

  <div align="center">
    <img alt="Captura de tela de site com muita informação, sem pistas de localização ao ações ao usuário, etc" src="https://user-images.githubusercontent.com/69374340/174390774-2dbc1b97-8dc0-47e5-afed-190e902a84a9.png">
  </div>

> **Observações:** pode causar confusão ao usuário por não facilitar a identificação de sua localização no site nem as ações permitidas claramente; não é minimalista, pelo contrário, utiliza exageradamente de informações e elementos na tela, causando cansaço mental ao interagir com o site e não estabelecendo harmonia visual; não há a presença de padrões, não há familiaridade do usuário com as funcionalidades disponíveis

</details>

---

## Aplicação dos conceitos de IHC no API

A partir de várias discussões com o professor Giuliano Bertoti, foi possível observar a aplicação de diversas heurísticas de Nielsen mas também conceitos do WCAG. Abaixo estão listadas algumas dessas observações:

<details>
   <summary><b>1. Visibilidade do status do sistema</b></summary>
    <br>
    Para sempre ter controle sobre o status do sistema e seus componentes, um dos mecanismos implementados no API foi o de exibir sempre o status do chamado em todas as telas relacionadas a ele (seja em listagens, como a da captura abaixo, ou em telas como "detalhes do chamado").

  <div align="center">
   <img alt="Tela home com os status de cada chamado na listagem" src="https://user-images.githubusercontent.com/69374340/174399624-76996515-6532-486a-aa4b-464637c9be2d.png">
  </div>
</details>

<details>
   <summary><b>3 Controle e liberdade para o usuário</b></summary>
    <br>
    Para conferir mais liberdade para o usuário, até mesmo como prevenção de erros, foi implementado algumas funcionalidades de alteração, atualização ou mesmo exclusão, como por exemplo a alteração da prioridade do chamado por parte de usuários suporte, como nas imagens a seguir:

<div align="center">

|                                                                                                          Detalhes do chamado                                                                                                          |                                                                     Alteração da prioridade do chamado                                                                      |
| :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| <img alt="Opção de alteração de prioridade do chamado na tela de detalhes do chamado visualizada por um usuário suporte" src="https://user-images.githubusercontent.com/69374340/174398967-8c2fa3d4-287c-4822-8aab-67ebbabf8581.png"> | <img alt="Dropdown para escolha da nova prioridade do chamado" src="https://user-images.githubusercontent.com/69374340/174399422-cf318d96-5a2d-4737-9640-99961c276218.png"> |

</div>

</details>

<details>
   <summary><b>4. Consistência e padronização & 8. Estética e degign minimalista</b></summary>
    <br>
    Com a finalidade de promover foco ao usuário, evitando telas com muitos elementos, ou componentes com animações e muitos efeitos visuais, adotamos uma estética minimalista ao sistema, além de padronizada, como no exemplo do formulário abaixo. Outros formulários do sistema, como cadastro de chamados ou de equipamentos, seguem o mesmo layout.

  <div align="center">
   <img alt="Cadastro de usuários com apenas o suficiente em tela para tal ação" src="https://user-images.githubusercontent.com/69374340/174398534-99ceafaa-8c7c-4683-bb4c-408e776d6295.png">
  </div>
</details>

<details>
   <summary><b>5. Prevenção de erros</b></summary>
    <br>
    Visando evitar erros, bem como avisar o usuário que a ação que ele está realizando não é correta, no API aplicamos um alerta caso ele tente realizar uma pesquisa em branco durante uma busca de uma palavra chave no centro de soluções, como na captura de tela abaixo:

  <div align="center">
    <img alt="Alerta para pesquisas em branco" src="https://user-images.githubusercontent.com/69374340/174397922-748c727d-c2ad-4ccb-a1e0-0bc636961b29.png">
  </div>
</details>
