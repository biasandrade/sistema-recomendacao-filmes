# sistema-recomendacao-filmes
🎬 Sistema de Recomendação de Filmes usando ML | Vetorização de texto, cosine similarity e NLP com Python

# 🎬 Sistema de Recomendação de Filmes

[![Python](https://img.shields.io/badge/Python-3.13-blue.svg)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.7.1-orange.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.3.0-green.svg)](https://pandas.pydata.org/)

Sistema de recomendação de filmes baseado em filtragem por conteúdo usando Machine Learning. O sistema analisa características de filmes (gênero, elenco, diretor, sinopse) e recomenda títulos similares através de vetorização de texto e cálculo de similaridade de cosseno.

## 🎯 Objetivo do Projeto

Construir um sistema inteligente que recomende 5 filmes similares ao que o usuário assistiu, mantendo-o engajado na plataforma. O projeto aplica conceitos de:
- Processamento de Linguagem Natural (NLP)
- Vetorização de texto
- Álgebra linear (espaço vetorial e distância de cosseno)
- Machine Learning não supervisionado

## 🔬 Metodologia

### 1. **Preparação dos Dados**
- Merge de datasets (filmes + elenco)
- Extração de features relevantes: gênero, palavras-chave, elenco principal (top 3), diretor
- Limpeza e remoção de valores ausentes

### 2. **Processamento de Texto (NLP)**
- **Stemming** com Porter Stemmer para redução de palavras à raiz
- Remoção de stop words em inglês (palavras comuns, com pouca informação)
- Normalização (lowercase, remoção de espaços)
- Concatenação de todas as features em uma única string (tags)

### 3. **Vetorização**
- **CountVectorizer** do scikit-learn com limite de 5000 features
- Transformação de texto em matriz numérica esparsa
- Cada filme representado como um vetor no espaço multidimensional

### 4. **Cálculo de Similaridade**
- **Cosine Similarity** para medir distância entre vetores
- Filmes com menor distância angular = maior similaridade
- Ranking dos 5 filmes mais próximos

## 📊 Dataset

- **Fonte**: [The Movie Database (TMDb)](https://developer.themoviedb.org/docs)
- **Registros**: 4.806 filmes
- **Features utilizadas**: 
  - `genres`, `keywords`, `cast`, `crew`, `overview`

## 🛠️ Tecnologias Utilizadas

```python
Python 3.13.5
├── pandas 2.3.0          # Manipulação de dados
├── numpy 2.3.1           # Computação numérica
├── scikit-learn 1.7.1    # Machine Learning
│   ├── CountVectorizer   # Vetorização
│   └── cosine_similarity # Distância de cosseno
└── nltk 3.9.1            # NLP e stemming
```

## 🚀 Como Usar

### Instalação

```bash
# Clone o repositório
git clone https://github.com/biasandrade/sistema-recomendacao-filmes.git

# Entre na pasta
cd sistema-recomendacao-filmes

# Instale as dependências
pip install -r requirements.txt
```

### Execução

Abra o Jupyter Notebook e execute todas as células:

```bash
jupyter notebook Projeto1_Filme_BeatrizAndrade.ipynb
```

### Exemplo de Uso

```python
# Recomendar filmes similares a "Avatar"
sistema_recomendacao('Avatar')

# Output:
# Aliens vs Predator: Requiem
# Aliens
# Falcon Rising
# Independence Day
# Titan A.E.
```

## 📈 Resultados

O sistema demonstrou alta precisão na recomendação de filmes similares:

| Filme Consultado | Top 5 Recomendações |
|------------------|---------------------|
| **Avengers: Age of Ultron** | Iron Man 3, Iron Man 2, Iron Man, Thor, The Avengers |
| **Jurassic World** | Jurassic Park, The Lost World, Walking With Dinosaurs, Terminator Genisys, Jurassic Park III |
| **Avatar** | Aliens vs Predator: Requiem, Aliens, Falcon Rising, Independence Day, Titan A.E. |

## 🧠 Conceitos Aplicados

### Matemática e Estatística
- Álgebra Linear (vetores e espaços vetoriais)
- Distância de cosseno
- Similaridade entre vetores multidimensionais

### Machine Learning
- Aprendizado não supervisionado
- Sistemas de recomendação baseados em conteúdo
- Feature engineering

### NLP
- Tokenização
- Stemming (Porter Stemmer)
- Bag of Words (BoW) (texto em números)
- TF (Term Frequency) (frequência da aparição da palavra)

## 📚 Aprendizados

Este projeto faz parte do curso **"Matemática e Estatística Aplicada Para Data Science, Machine Learning e IA"** da Data Science Academy, onde apliquei conceitos de:

✅ Vetorização de texto  
✅ Processamento de linguagem natural  
✅ Cálculo de similaridade  
✅ Sistemas de recomendação  
✅ Feature engineering  

## 🔮 Melhorias Futuras

- [ ] Implementar filtro colaborativo (user-based)
- [ ] Adicionar ponderação TF-IDF (frequência e raridade da aparição da palavra)? (Talvez)
- [ ] Interface web com Streamlit
- [ ] Incluir avaliações de usuários (ratings)

## 👩‍💻 Autora

**Beatriz Andrade**  
Cientista de Dados | 18 anos de experiência com análise de dados

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Beatriz%20Andrade-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/andrade-beatriz/)
[![Email](https://img.shields.io/badge/Email-biasandrade%40gmail.com-red?style=flat&logo=gmail)](mailto:biasandrade@gmail.com)

## 📄 Licença

Este projeto está sob a licença MIT. Sinta-se livre para usar, modificar e distribuir.

---

⭐ Se este projeto te ajudou, considere dar uma estrela no repositório!
