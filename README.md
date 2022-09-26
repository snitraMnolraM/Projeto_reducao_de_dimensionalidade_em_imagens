# Projeto_reducao_de_dimensionalidade_em_imagens
Realizando a implementação em Python para transformar uma imagem colorida para níveis de cinza (0 a 255) e para binarizada (0 e 255), preto e branco.



Redução de dimensão no espaço de cor: 

Espera-se usar o número reduzido de tons de cinza, preservando o máximo possível, o contraste da imagem original. Inevitavelmente há perdas de informação de cor. 

[ ]()![img](data:image/jpg;base64, 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)

A redução de dimensionalidade é um processo que tem por objetivo diminuir o número de variáveis — ou dimensões — de um conjunto de dados (*dataset*) visando a menor perda de informações possível.



Há diversas razões pelas quais trabalhar com um dataset dotado de um número grande de features, isto é, com muitas dimensões, pode se configurar em uma desvantagem. Em primeira instância, vale ressaltar que quanto maior o número de features, maior também o número de amostras necessárias. Isso porque, nessa condição, é preciso um número maior delas para ter um dataset plural o suficiente para contemplar todas as possíveis combinações de features, a fim de possibilitar a construção de modelos generalistas. Este fenômeno é chamado de *Maldição da Dimensionalidade.*

As técnicas de redução de dimensionalidade têm vasta aplicação, já que podem ser utilizadas em qualquer contexto no qual haja dezenas, centenas ou até mesmo milhares de features a serem analisadas e processadas em um único conjunto de dados. Dados do mundo real, como sinais de fala, fotografias digitais ou imagens por ressonância magnética funcional (fMRI), geralmente possuem alta dimensionalidade e para manusear esses dados reais adequadamente, a sua dimensionalidade deve ser reduzida (VAN DER MAATEN; POSTMA; VAN DEN HERIK, 2009). Sendo assim, as técnicas de redução — lineares ou, mais recentemente, não lineares — são especialmente utilizadas para o processamento de sinais, reconhecimento de voz, neuroinformática e bioinformática.



Nesse projeto  usamos a imagem da Lena

![resultado.jpg](https://github.com/snitraMnolraM/Projeto_reducao_de_dimensionalidade_em_imagens/blob/main/img/resultado.jpg?raw=true)





