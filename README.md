# 🎵 Análise da Retrospectiva Spotify 2024  

Este projeto tem como objetivo explorar e visualizar os dados de escuta de música no Spotify, buscando identificar discrepâncias entre os dados fornecidos pela plataforma e os dados reais de consumo. A análise visa fornecer insights sobre o consumo de conteúdo, os artistas mais ouvidos e os períodos de escuta mais intensos, permitindo uma retrospectiva mais precisa e alinhada com as expectativas do usuário.  

**Mais detalhes da análise do projeto aqui:**  
[spotify_retrospectiva_2024.ipynb](https://github.com/hian-stafford/retrospectiva_spotify_2024/blob/main/spotify_retrospectiva_2024.ipynb)  

## 📆 Até Quando o Spotify Monitora os Dados para o Wrapped?  

- **Início do monitoramento**: 1º de janeiro, conforme relatado em [post no Reddit](https://www.reddit.com/r/truespotify/comments/187v8oc/is_spotify_already_collecting_data_for_spotify/?tl=pt-br).  
- **Prazo final para 2024**: Anteriormente, o Spotify utilizava os dados até 15 de novembro, mas, em 2024, esse prazo foi estendido para 20 de novembro.  
- Essa alteração está associada ao comunicado aos artistas sobre o envio de vídeos curtos para fãs, parte do Wrapped:  
  > "Estendemos o prazo para os Clips do Wrapped 2024 até 20 de novembro. Não perca a chance de compartilhar esse momento especial com seus maiores fãs!”  
- Após o Wrapped, os Clips continuarão disponíveis na página dos artistas, na visualização do Now Playing e nas áreas de capa.  
- Fonte: [NSC Total](https://www.nsctotal.com.br/noticias/spotify-wrapped-2024-quando-sai-e-tudo-sobre-a-retrospectiva#:~:text=Até%20quando%20o%20Spotify%20faz,que%20os%20ouvintes%20continuem%20curtindo).  

## 🎯 Objetivos  

- Explorar e visualizar os dados de escuta de música no Spotify.  
- Identificar discrepâncias entre os dados fornecidos pela plataforma e os dados reais de consumo.  
- Obter insights sobre:  
  - Consumo de conteúdo.  
  - Artistas mais ouvidos.  
  - Períodos de escuta mais intensos.  

## 📊 Descrição dos Dados  

Os dados utilizados neste projeto são registros extraídos da conta pessoal do Spotify, contendo as seguintes informações:  

- **`ts`**: Carimbo de data/hora indicando quando a faixa parou de ser tocada (formato UTC, horário militar).  
- **`ms_played`**: Duração do streaming em milissegundos.  
- **`master_metadata_track_name`**: Nome da faixa.  
- **`master_metadata_album_artist_name`**: Nome do artista, banda ou podcast.  
- **`reason_start`**: Motivo da reprodução, como:  
  - `trackdone`: Faixa concluída.  
  - `clickrow`: Clique na linha.  
  - `fwdbtn`: Botão de avanço.  
  - `backbtn`: Botão de retrocesso.  
  - `remote`: Remoto.  
  - `appload`: Carregamento da faixa.  

## 🔍 Metodologia  

1. **Conversão de dados**: Transformação do tempo de reprodução de milissegundos para minutos, facilitando a análise.  
2. **Agregação**: Agrupamento dos dados por dia e por artista para identificar padrões de consumo.  
3. **Manipulação de dados**:  
   - Uso da biblioteca `pandas` para filtragem, transformação e agrupamento.  
   - Contabilização dos minutos de reprodução por artista e por faixa.  
4. **Visualização de dados**:  
   - Uso de `matplotlib` para criar gráficos e explorar a evolução dos minutos escutados.  
   - Adição de estilos aprimorados com `seaborn`.  
5. **Técnicas de agrupamento**: Identificação dos 100 artistas mais ouvidos e dos minutos acumulados de reprodução.  

## 📈 Resultados Esperados e Insights  

- Proporcionar uma retrospectiva personalizada, validando ou refutando informações apresentadas pelo Spotify Wrapped.  
- Identificar padrões de consumo, como dias de maior intensidade musical e artistas predominantes.  
- Explorar eventos que influenciaram o aumento no tempo de reprodução, como lançamentos de álbuns e singles.  
- Destacar mudanças no comportamento de escuta ao longo do tempo.  

## 🔧 Ferramentas e Tecnologias Utilizadas  

- **Bibliotecas Python**:  
  - `pandas`: Manipulação de dados.  
  - `matplotlib` e `seaborn`: Criação de gráficos e visualizações.  
- **Ambiente**: Jupyter Notebook.  

## 📝 Conclusão e Próximos Passos  

A análise dos dados revelou discrepâncias entre os dados reais de consumo e os apresentados pelo Spotify Wrapped. Essas inconsistências reforçam a importância de validar informações oferecidas por plataformas.  

### Próximos Passos:  

- Realizar análises mais aprofundadas sobre padrões sazonais e eventos específicos.  
- Comparar os dados de consumo com informações fornecidas por outras plataformas de streaming.  
- Expandir a análise para dados de múltiplos usuários, identificando tendências gerais.  

---

💡 **Contribuições são bem-vindas!** Caso queira contribuir, sinta-se à vontade para abrir issues ou enviar pull requests.  
