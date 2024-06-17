# ponderada-S9
# Ferramentas de PLN na AWS

Este documento apresenta um levantamento das ferramentas de Processamento de Linguagem Natural (PLN) disponíveis na AWS (Amazon Web Services), incluindo exemplos de aplicações de cada serviço.

## Amazon Comprehend

**Descrição**: O Amazon Comprehend é um serviço de PLN que utiliza machine learning para descobrir insights e relações em textos.

**Exemplo de aplicação**: Análise de sentimentos em comentários de clientes para determinar as opiniões positivas e negativas.

```http
POST /comprehend/v1/detect-sentiment
Host: comprehend.amazonaws.com
Content-Type: application/json

{
  "Text": "Mano Hayas, me dá um help pf!",
  "LanguageCode": "pt"
}
```

## Amazon Translate

**Descrição**: O Amazon Translate é um serviço de tradução automática que usa modelos avançados de machine learning para fornecer traduções rápidas e precisas.

**Exemplo de aplicação**: Tradução de websites ou documentos de negócios para facilitar a comunicação internacional.

```http
POST /translate/v1/text
Host: translate.amazonaws.com
Content-Type: application/json

{
  "Text": "Duvido vc me dar um 10 nessa ponderada",
  "SourceLanguageCode": "pt",
  "TargetLanguageCode": "en"
}
```

## Amazon Transcribe

**Descrição**: O Amazon Transcribe usa tecnologias avançadas de aprendizado de máquina para converter fala em texto precisamente.

**Exemplo de aplicação**: Transcrição de chamadas de serviço ao cliente para análise subsequente e treinamento de representantes.

```http
POST /transcribe/v1/start-transcription-job
Host: transcribe.amazonaws.com
Content-Type: application/json

{
  "Media": {
    "MediaFileUri": "s3://meu-bucket-de-audio/audio.mp3"
  },
  "LanguageCode": "pt-BR",
  "MediaFormat": "mp3"
}
```

## Conclusão

Estes são apenas alguns dos serviços de PLN oferecidos pela AWS. Cada um destes serviços pode ser acessado e gerenciado via HTTP, proporcionando flexibilidade para integração com diversas aplicações.
