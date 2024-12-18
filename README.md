# Geração de Imagens com DALL·E 3 via OpenAI API

Este repositório contém um projeto que utiliza a API da OpenAI para gerar imagens com o modelo **DALL·E 3**, baseando-se em prompts textuais. Ele foi projetado para automatizar o processo de geração de imagens e salvamento de imagens localmente.

## Funcionalidades

- Geração automática de imagens a partir de prompts textuais.
- Utilização do modelo **DALL·E 3** para criar imagens de alta qualidade.
- Armazenamento das imagens geradas em formato `.png` com nomes numerados sequencialmente.

## Pré-requisitos

Antes de começar, certifique-se de que você tenha:

1. Uma conta na OpenAI com acesso à API do DALL·E 3.
2. A chave de API fornecida pela OpenAI.
3. Python 3.7+ instalado em sua máquina.
4. As bibliotecas Python necessárias instaladas:
   - `openai`
   - `requests`

## Como Usar

1. Clone este repositório:
   ```bash
   git clone https://github.com/JunioVeras/TCC.git
   cd TCC
   ```

2. Instale as dependências:
   ```bash
   pip install openai requests
   ```

3. Configure sua chave de API:
   - Certifique-se de que a variável de ambiente `OPENAI_API_KEY` contém sua chave de API:
     ```bash
     export OPENAI_API_KEY="sua_chave_de_api_aqui"
     ```

     ou crie um arquivo .env no mesmo diretório com a chade de API

4. Execute o script:
   - Edite o prompt no arquivo `image_generator.ipynb` para o texto que deseja gerar imagens.
   - Execute o notebook para gerar as imagens

5. As imagens geradas serão salvas no diretório raíz.

## Observações

- O script é configurado para gerar 20 imagens por execução, mas este número pode ser ajustado alterando a variável `num_images`.
- Certifique-se de que a API da OpenAI está disponível e ativa antes de executar o script.
- O uso excessivo da API pode acarretar custos; verifique os limites e preços na [documentação oficial da OpenAI](https://platform.openai.com/docs/).

---

**Autor:** Júnio Veras
