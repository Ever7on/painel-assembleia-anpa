# Painel da Assembleia Ordinária · ANPa

Painel de tarefas da equipe de comunicação da Associação Norte do Pará para a cobertura da XIX Assembleia Ordinária (20 a 22 de novembro de 2026), com o tema "À Luz da Palavra".

O site é publicado pelo GitHub Pages. Os status, as datas e as notas das tarefas ficam no Firebase (Cloud Firestore) e são atualizados em tempo real para toda a equipe.

## Arquivos

| Arquivo | Para que serve |
| --- | --- |
| `index.html` | O painel |
| `firebase-config.js` | Configuração do projeto Firebase |
| `tarefas.json` | Lista inicial das tarefas, usada só na primeira importação |
| `atualizacoes.json` | Ajustes nas tarefas já salvas no Firebase, aplicados uma vez por revisão |
| `detalhes.json` | O "como fazer" de cada tarefa, mostrado no botão Como fazer |
| `firestore.rules` | Regras de acesso do banco de dados |
| `fonts/ChettaVissto.ttf` | Fonte da identidade visual |

## Como ligar ao Firebase

1. Em [console.firebase.google.com](https://console.firebase.google.com), crie um projeto. O Google Analytics pode ficar desligado.
2. Abra **Firestore Database**, clique em **Criar banco de dados**, escolha o local `southamerica-east1` (São Paulo) e o **modo de produção**.
3. Na aba **Regras**, cole o conteúdo de `firestore.rules` e clique em **Publicar**.
4. Em **Configurações do projeto > Seus apps**, adicione um app da Web (ícone `</>`) e copie o objeto `firebaseConfig` para `firebase-config.js`.
5. Abra o painel e clique em **Importar tarefas do cronograma** (só na primeira vez).

A configuração do Firebase não é uma senha: ela fica visível no site, e o acesso é controlado pelas regras do Firestore.

## Acesso

Qualquer pessoa com o link pode ver o painel e atualizar status, datas e notas. Ninguém consegue apagar tarefas pelo site. Compartilhe o link só com a equipe.
