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

## 🛠️ Como Baixar Seus Dados Pessoais do Spotify  

Se você deseja utilizar seus próprios dados no projeto, o Spotify permite que os usuários baixem seus dados pessoais por meio de sua plataforma. Siga os passos abaixo para obter os dados:  

### Passo 1: Solicitar os Dados no Spotify  

1. Acesse o site oficial do Spotify: [www.spotify.com](https://www.spotify.com).  
2. Faça login em sua conta.  
3. No menu superior direito, clique em **Perfil** > **Conta**.  
4. Na página da conta, localize a seção **Configurações de Privacidade**.  
5. Clique em **Baixar seus dados**.  
6. Escolha os tipos de dados que deseja solicitar. Certifique-se de incluir os históricos de reprodução (streaming history).  
7. Confirme a solicitação.  

> **Nota**: O Spotify pode levar até 30 dias para processar a solicitação e enviar os dados para o seu e-mail registrado.  

### Passo 2: Receber e Baixar os Dados  

1. Quando os dados estiverem prontos, você receberá um e-mail do Spotify com um link para download.  
2. Clique no link do e-mail e faça o download dos dados.  
3. O download será fornecido como um arquivo `.zip`. Extraia o conteúdo para acessar os arquivos.  

### Passo 3: Encontrar o Arquivo de Histórico de Streaming  

1. Dentro da pasta extraída, localize o arquivo chamado `StreamingHistory.json` (ou similar).  
2. Este arquivo contém informações detalhadas sobre suas músicas ouvidas, incluindo artista, faixa, duração e timestamps.  

### Passo 4: Preparar os Dados para Análise  

Antes de usar os dados no projeto, certifique-se de que o arquivo JSON está acessível. Copie o arquivo para o mesmo diretório do notebook ou ajuste o caminho no código conforme necessário:  

```python
# Exemplo de carregamento do arquivo
import pandas as pd

# Carregar os dados do JSON
df = pd.read_json("Streaming_History_Audio_2023-2024.json")
df.head(10)
