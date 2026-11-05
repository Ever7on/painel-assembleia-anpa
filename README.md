# Painel da Assembleia Ordinária · ANPa

Painel de tarefas da equipe de comunicação da Associação Norte do Pará para a cobertura da XIX Assembleia Ordinária (20 a 22 de novembro de 2026), com o tema "À Luz da Palavra".

O site é publicado pelo GitHub Pages. Os status, as datas e as notas das tarefas ficam no Firebase (Cloud Firestore) e são atualizados em tempo real para toda a equipe.

## Arquivos

| Arquivo | Para que serve |
| --- | --- |
| `index.html` | O painel |
| `firebase-config.js` | Configuração do projeto Firebase |
| `tarefas.json` | Lista inicial das tarefas, usada só na primeira importação |
| `firestore.rules` | Regras de acesso do banco de dados |
| `fonts/ChettaVissto.ttf` | Fonte da identidade visual |

## Como ligar ao Firebase

1. Em [console.firebase.google.com](https://console.firebase.google.com), crie um projeto (ex.: `painel-assembleia-anpa`). O Google Analytics é opcional.
2. Em **Criação > Authentication > Método de login**, ative o provedor **Anônimo**.
3. Em **Criação > Firestore Database**, crie o banco no modo de produção (local `southamerica-east1`, em São Paulo).
4. Ainda no Firestore, na aba **Regras**, cole o conteúdo de `firestore.rules` e clique em **Publicar**.
5. Em **Configurações do projeto > Geral > Seus apps**, adicione um app da Web e copie o objeto `firebaseConfig`.
6. Cole esses valores em `firebase-config.js`.
7. Em **Authentication > Configurações > Domínios autorizados**, adicione `SEU-USUARIO.github.io`.
8. Abra o painel. Na primeira vez, ele mostra o botão **Importar tarefas do cronograma**, que carrega as tarefas de `tarefas.json`.

A configuração do Firebase não é uma senha: ela fica visível no site, e o acesso é controlado pelas regras do Firestore.

## Acesso

Qualquer pessoa com o link pode ver o painel e atualizar status, datas e notas. Ninguém consegue apagar tarefas pelo site. Compartilhe o link só com a equipe.
