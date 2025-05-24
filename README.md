# Geração e Análise de Imagens com Modelos de IA (DALL·E 3, Imagen 3 e Stable Diffusion)

Este repositório contém um projeto de TCC que utiliza três modelos de geração de imagens baseados em IA — **DALL·E 3 (OpenAI)**, **Imagen 3 (Google)** e **Stable Diffusion 3.5 (Stability AI)** — para produzir imagens com base em prompts textuais. Além disso, o projeto inclui um módulo de **análise de similaridade** das imagens utilizando o modelo **CLIP** da OpenAI (via OpenCLIP).

## Funcionalidades

- ✅ Geração automática de imagens com base em uma lista de prompts em português e inglês.  
- ✅ Suporte aos modelos DALL·E 3, Imagen 3 e Stable Diffusion 3.5.  
- ✅ Organização das imagens em diretórios separados por prompt e por modelo.  
- ✅ Comparação e análise de similaridade entre imagens utilizando embeddings do modelo CLIP.  
- ✅ Suporte a diferentes formatos de imagem (`.png` e `.jpg`).  
- ✅ Pré-processamento automatizado de imagens para cálculo de embeddings.  
- ✅ Armazenamento local das imagens com nomes numerados sequencialmente.  

## Pré-requisitos

Antes de começar, certifique-se de que você tenha:

1. Conta e **chave de API** válidas para:
   - [OpenAI (DALL·E 3)](https://platform.openai.com/)
   - [Google AI (Imagen 3)](https://ai.google.dev/gemini-api/)
   - [Stability AI (Stable Diffusion)](https://platform.stability.ai/docs/api-reference)
   
2. Python 3.7 ou superior.
3. Bibliotecas Python instaladas:
```bash
pip install openai requests google-generativeai torch torchvision open-clip-torch matplotlib scikit-learn tqdm python-dotenv
```

## Como Usar

1. Clone este repositório:
   ```bash
   git clone https://github.com/JunioVeras/TCC.git
   cd TCC
   ```

2. Instale as dependências:
   ```bash
   pip install openai requests google-generativeai torch torchvision open-clip-torch matplotlib scikit-learn tqdm python-dotenv
   ```

3. Configure as variáveis de ambiente com as chaves de API:
   - Certifique-se de que as variáveis de ambiente `OPENAI_API_KEY`, `GOOGLE_AI_API_KEY` e `STABLE_DIFFUSION_API_KEY` contenham suas chaves de API:
     ```bash
     export OPENAI_API_KEY="sua_chave_de_api_aqui"
     ```

     ou crie um arquivo .env no mesmo diretório com as chave de API
      ```env
      OPENAI_API_KEY=chave_openai
      GOOGLE_AI_API_KEY=chave_google
      STABLE_DIFFUSION_API_KEY=chave_stability
      ```

4. Execute o script:
   
   Abra e execute o notebook image_generator.ipynb:
   - O script irá gerar imagens para 17 prompts diferentes, utilizando os 3 modelos.
   - As imagens serão salvas em diretórios como DALLE_3/, IMAGEN_3/ e STABLE_DIFFUSION_3_5/, separados por categorias como UmCarnavalBrasileiro/, UmaCidadeBrasileira/ etc.

5. Calcule a similaridade:
   
   Abra e execute o notebook similarity_calculator.ipynb para:
   - Extrair embeddings CLIP das imagens geradas.
   - Comparar imagens por prompt entre os diferentes modelos.
   - Realizar análises quantitativa de similaridade visual

## Estrutura de Diretórios
```
TCC/
├── DALLE_3/
│   ├── UmCarnavalBrasileiro/
│   └── ...
├── IMAGEN_3/
│   ├── UmCarnavalBrasileiro/
│   └── ...
├── STABLE_DIFFUSION_3_5/
│   ├── UmCarnavalBrasileiro/
│   └── ...
├── image_generator.ipynb
├── similarity_calculator.ipynb
└── .env
```
## Observações

- O número de imagens geradas por prompt pode ser ajustado na variável num_images.
- O tempo entre requisições foi configurado para respeitar os limites das APIs.
- O uso excessivo da API pode acarretar custos. Consulte as documentações oficiais para mais detalhes:
   - [OpenAI (DALL·E 3)](https://platform.openai.com/)
   - [Google AI (Imagen 3)](https://ai.google.dev/gemini-api/)
   - [Stability AI (Stable Diffusion)](https://platform.stability.ai/docs/api-reference)

---

**Autor:** Júnio Veras
