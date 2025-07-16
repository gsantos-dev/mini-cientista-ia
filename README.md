# 🧠 Mini Cientista IA

Este repositório contém um **assistente inteligente de pesquisa científica** que busca, analisa e organiza artigos da base **PubMed** com o auxílio de uma IA baseada em **modelos de linguagem** (LLMs).

## 🔬 Sobre o projeto

O **Mini Cientista IA** é uma solução automatizada e inteligente que transforma a forma como pesquisadores, estudantes e profissionais da saúde acessam e interpretam informações científicas.

Projetado para lidar com grandes volumes de dados da base PubMed, o sistema permite a busca precisa de artigos científicos em inglês sobre qualquer tema de interesse (ex: _whey protein_), realiza o **download e leitura automatizada dos abstracts** e, com o apoio de um **modelo de linguagem da OpenAI**, executa **resumos contextuais, objetivos e bem estruturados**.

Esse processo reduz drasticamente o tempo necessário para revisão bibliográfica, ao mesmo tempo que mantém a qualidade e relevância dos conteúdos extraídos. Os resultados são organizados e exportados em formato `.docx` de forma clara, prontos para uso em relatórios, apresentações, pesquisas ou TCCs.

Principais destaques:
- Automatiza tarefas repetitivas e demoradas de pesquisa científica.
- Garante clareza nos resumos com uso de IA.
- Exporta automaticamente os resultados prontos para uso.
- Código modular e facilmente adaptável a outras bases e domínios científicos.

---

## 📂 Estrutura do Projeto

```
mini-cientista-ia/
├── Agent_PubMed_OFICIAL.ipynb    # Notebook principal com todo o fluxo de busca e resumo
├── LICENSE                       # Licença Apache 2.0
├── README.md                     # Este documento
```

---

## ⚙️ Instalação

1. Clone o repositório:

```bash
git clone https://github.com/gsantos-dev/mini-cientista-ia.git
cd mini-cientista-ia
```

2. Crie um ambiente virtual (opcional, mas recomendado):

```bash
python -m venv venv
venv\Scripts\activate
```

3. Instale as dependências:

```bash
pip install -r requirements.txt
```

4. Crie um arquivo `.env` com sua chave da OpenAI:

```
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

---

## 🧪 Como usar

1. Abra o arquivo `Agent_PubMed_OFICIAL.ipynb` em um ambiente como **Jupyter Notebook** ou **VSCode**.
2. Execute as células sequencialmente.
3. O resultado será um conjunto de resumos de artigos científicos relacionados ao termo pesquisado.

---

## 🔁 Alterar o termo da pesquisa

Por padrão, o notebook está configurado para pesquisar **"whey protein"**.  
Caso deseje pesquisar sobre outro tema, localize esta parte do código no notebook:

```python
topics = [
    "Whey Protein adverse effects"
]
```

E substitua pelo termo desejado, como:

```python
topics = [
    "Vitamin D deficiency in children"
]
```

Você pode usar **um ou mais termos**. Basta adicionar à lista:

```python
topics = [
    "Vitamin D deficiency",
    "Iron supplementation in athletes"
]
```

---

## 📌 Dependências principais

- [`Bio.Entrez`](https://biopython.org/) – para consulta à PubMed
- [`LangChain`](https://python.langchain.com) – para orquestrar chamadas à IA
- [`OpenAI`](https://platform.openai.com/) – modelo de linguagem para resumo
- `dotenv`, `pandas`, `docx`, `re` – para organização, exportação e utilidades

---

## 🛡️ Licença

Este projeto está licenciado sob a [Apache License 2.0](LICENSE).

---

## 🙋‍♂️ Autor

Desenvolvido por **Guilherme Santos Pereira**  
📫 [github.com/gsantos-dev](https://github.com/gsantos-dev)

---

## 🚀 Dica: Este projeto é ideal para pesquisadores, estudantes e profissionais que precisam de uma forma rápida e eficiente de analisar literatura científica!
