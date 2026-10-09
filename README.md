# ximovissa

Site de recrutamento de motoristas XIMOVISSA. Contacto oficial: **+258 85 396 5084**.

## Ficheiros

- `index.html`: site completo, com estilos, formulário e carros em 3D incorporados.
- `vercel.json`: configuração para servir o site estático sem instalação nem compilação.
- `README.md`: este guia de publicação.
- `motorista-junto-ao-carro.webp`, `motorista-ao-volante.webp` e `motorista-com-chaves.webp`: imagens da campanha de recrutamento, servidas pelo próprio site e carregadas apenas quando necessárias.

As três imagens publicitárias foram geradas com a ferramenta de imagem incorporada. Direção da campanha: motorista africano com camisa e chapéu azuis, marca XIMOVISSA bordada em branco e carro branco; cenas junto ao carro, ao volante com cinto de segurança e com as chaves na mão. Foram convertidas para WebP para reduzir o tamanho sem alterar a composição.

Não é necessário instalar Node.js, executar npm ou configurar variáveis de ambiente. As fontes são carregadas pelo Google Fonts; existem fontes de sistema como alternativa se a ligação falhar. A animação não depende de ficheiros ou bibliotecas externas.

## Publicar no GitHub

1. Abra https://github.com/new?name=ximovissa e crie o repositório `ximovissa` na conta pretendida. Pode manter o repositório privado e publicar o site pela Vercel.
2. Descompacte `ximovissa.zip` e abra a pasta `ximovissa`.
3. No GitHub, escolha **Add file → Upload files**. Num repositório vazio, use **uploading an existing file**.
4. Carregue os seis ficheiros diretamente na raiz do repositório, incluindo as três imagens WebP. Não carregue apenas o ZIP nem coloque os ficheiros dentro de outra pasta `ximovissa`.
5. Confirme o envio com **Commit changes**.

## Publicar na Vercel

1. Entre em https://vercel.com/new e ligue a conta GitHub.
2. Importe o repositório `ximovissa`.
3. Use **ximovissa** em **Project Name**.
4. Mantenha **Root Directory** na raiz do repositório.
5. A configuração em `vercel.json` define automaticamente os valores abaixo:

| Campo | Valor |
| --- | --- |
| Framework Preset | Other |
| Build Command | Vazio |
| Install Command | Vazio |
| Output Directory | . |

6. Clique em **Deploy** e use o endereço real atribuído pela Vercel. O nome de projeto não garante a disponibilidade de um domínio específico.

Depois de ligar o repositório, os novos commits na branch de produção passam pelo processo de publicação da Vercel.

## Verificações realizadas

- Os 11 botões de categoria marcam e desmarcam escolhas.
- A seleção múltipla sincroniza as categorias acima do formulário e no cadastro.
- As escolhas permanecem ao voltar e avançar nas etapas.
- O resumo e a mensagem preparada para o WhatsApp incluem as categorias selecionadas.
- Os dois seletores incluem as 10 províncias e Cidade de Maputo.
- A opção `Outra` apresenta e valida o campo adicional.
- Os campos obrigatórios impedem o avanço sem os dados necessários.
- Os contactos apontam para `258853965084`.
- A animação dos carros continua sem botão de pausa.
- Não existem IDs duplicados nem destinos internos em falta; o JavaScript passa na verificação de sintaxe.

Estes testes verificam a lógica no DOM e o desenho no canvas. Não substituem a verificação visual e de toque num navegador real. Após publicar, teste no iPhone/Android e num computador: escolha duas categorias, preencha o cadastro, volte uma etapa e confirme a mensagem preparada no WhatsApp. Esta operação deve abrir uma mensagem para revisão; envie-a apenas quando pretender.

## Como funciona a candidatura

O site prepara os dados e abre a conversa no WhatsApp. O candidato precisa enviar a mensagem para a candidatura chegar à equipa. O site não guarda candidaturas numa base de dados, não envia mensagens sozinho e não possui painel administrativo nem upload de documentos.

## Referências oficiais

- Vercel — configuração do build: https://vercel.com/docs/builds/configure-a-build
- Vercel — vercel.json: https://vercel.com/docs/project-configuration/vercel-json
- GitHub — criar um repositório: https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository
- GitHub — carregar ficheiros: https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository
