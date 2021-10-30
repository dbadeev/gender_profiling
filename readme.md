# Одножанровое и многожанровое гендерное профилирование авторов по набору текстов соцсетей

## Питч-видеоотчет ##

<a href="https://disk.yandex.ru/i/bnDQcSYbAYV_mw" target="_blank"><img src="https://github.com/dbadeev/gender_profiling/blob/main/images/gender_profiling.png" 
alt="Видеоотчет" width="240" height="180" border="10" /></a>

  
##  

## Основные результаты и сравнение


                                    One-genre Gender Detection (Russian)
| Work                     | Publishing Year | Corpus                                  | Features                                                                         | Method used       | Result |
| ------------------------ | --------------- | --------------------------------------- | -------------------------------------------------------------------------------- | ----------------- | ------ |
| <b>RuSb_base+stylometry     |                 | PAN FIRE ’17 [d8]                       | Stylometric features                                                             | Russsian SBERT    | <b>0.90   |
| <b>RuSb_base                |                 | PAN FIRE ’17 [d8]                       |                                                                                  | Russsian SBERT    | <b>0.87   |
| Korshunov [r6]           | 2013            | self-made                               | word (3-grams)                                                                   | SVM               | 0.86   |
| Sboev et al [r4]         | 2019            | RusProfilihg [d11]<br>PAN FIRE ’17 [d8] | char n-grams                                                                     | Gradient Boosting | 0.79   |
| Сбоев и др. [r1]         | 2020            | LiveJournal [d10]                       |                                                                                  | GRU, CVAE         | 0.76   |
| Markov et al - CIC3 [r2] | 2017            | PAN FIRE ’17 [d8]                       | statistical                                                                      |                   | 0.6825 |
| LDR [d12]                | 2017            | PAN FIRE ’17 [d8]                       | probability distribution of occurrence of tdoc’s words in the different classes. |                   | 0.6759 |
| Markov et al - CIC2 [r2] | 2017            | PAN FIRE ’17 [d8]                       | BOW, word (suffix 3-grams), tf-idf                                               | SVM               | 0.6650 |
| Bhargava et al [r3]      | 2017            | PAN FIRE ’17 [d8]                       | POS, rule-based classification                                                   | LSTM, Bi-LSTM     | 0.6525 |
| Markov et al - CIC1 [r2] | 2017            | PAN FIRE ’17 [d8]                       | POS combination, tf-idf                                                          | SVM               | 0.6525 |


                                    Cross-genre Gender Detection (Russian)

| Work                     | Publishing Year | Corpus                                    | Features                                                  | Method used       | Test Corpus      | Result |
| ------------------------ | --------------- | ----------------------------------------- | --------------------------------------------------------- | ----------------- | ---------------- | ------ |
|<b>RuSb_base+stylometry    |                 | PAN FIRE ’17 [d8]<br>(Twitter - training) | Stylometric features                                      | Russsian SBERT    | Essays           | <b>0.87   |
| <b>RuSb_base                |                 | PAN FIRE ’17 [d8]<br>(Twitter - training) |                                                           | Russsian SBERT    | Essays           | <b>0.86   |
| <b>RuSb_big                 |                 | RusProfilihg [d11]<br>PAN FIRE ’17 [d8]   |                                                           | Russsian SBERT    | Essays           | <b>0.86   |
| <b>RuSb_big+stylometry      |                 | RusProfilihg [d11]<br>PAN FIRE ’17 [d8]   | Stylometric features                                      | Russsian SBERT    | Essays           | <b>0.86   |
| LDR [d12]                | 2017            | PAN FIRE ’17 [d8]<br>(Twitter - training) | stylometric analysis                                      |                   | Essays           | 0.8141 |
| Bhargava et al [r3]      | 2017            | PAN FIRE ’17 [d8]<br>(Twitter - training) | POS, rule-based classification                            | LSTM, Bi-LSTM     | Essays           | 0.7838 |
| Vinayan et al [r5]       | 2017            | PAN FIRE ’17 [d8]<br>(Twitter - training) | exotic stat (average word length, URL usage, etc), tf-idf | SVM               | Essays           | 0.6811 |
| <b>RuSb_big+stylometry      |                 | RusProfilihg [d11]<br>PAN FIRE ’17 [d8]   | Stylometric features                                      | Russsian SBERT    | Reviews          | <b>0.83   |
| <b>RuSb_big                 |                 | RusProfilihg [d11]<br>PAN FIRE ’17 [d8]   |                                                           | Russsian SBERT    | Reviews          | <b>0.83   |
| <b>RuSb_base+stylometry     |                 | PAN FIRE ’17 [d8]<br>(Twitter - training) | Stylometric features                                      | Russsian SBERT    | Reviews          | <b>0.80   |
| <b>RuSb_base                |                 | PAN FIRE ’17 [d8]<br>(Twitter - training) |                                                           | Russsian SBERT    | Reviews          | <b>0.80   |
| Sboev et al [r4]         | 2019            | PAN FIRE ’17 [d8]<br>(Twitter - training) | char n-grams                                              | Gradient Boosting | Reviews          | 0.79   |
| LDR [d12]                | 2017            | PAN FIRE ’17 [d8]<br>(Twitter - training) | stylometric analysis                                      |                   | Reviews          | 0.72   |
| Markov et al - CIC3 [r2] | 2017            | PAN FIRE ’17 [d8]<br>(Twitter - training) | statistical                                               |                   | Reviews          | 0.6186 |
| Markov et al - CIC1 [r2] | 2017            | PAN FIRE ’17 [d8]<br>(Twitter - training) | POS combination, tf-idf                                   | SVM               | Reviews          | 0.5979 |
| Bhargava et al [r3]      | 2017            | PAN FIRE ’17 [d8]<br>(Twitter - training) | POS, rule-based classification                            | LSTM, Bi-LSTM     | Reviews          | 0.5786 |
| <b>RuSb_big                 |                 | PAN FIRE ’17 [d8]<br>(Twitter - training) |                                                           | Russsian SBERT    | Gender imitation | <b>0.95   |
| <b>RuSb_base                |                 | PAN FIRE ’17 [d8]<br>(Twitter - training) |                                                           | Russsian SBERT    | Gender imitation | <b>0.93   |
| Bhargava et al [r3]      | 2017            | PAN FIRE ’17 [d8]<br>(Twitter - training) | POS, rule-based classification                            | LSTM, Bi-LSTM     | Gender imitation | 0.6596 |
| LDR [d12]                | 2017            | PAN FIRE ’17 [d8]<br>(Twitter - training) | stylometric analysis                                      |                   | Gender imitation | 0.6383 |

##

### Отчет о проекте
<a href="https://paper.dropbox.com/doc/Gender-Profiling-in-Social-Network--BP2ohluKRa02VZ1Ob0MZjSuxAg-SMGmfj5PZC3b9P9Uvx6jm" target="_blank"><img src="https://github.com/dbadeev/gender_profiling/blob/main/images/gender_profiling_report.png" 
alt="Отчет о проекте" width="240" height="180" border="10" /></a>

