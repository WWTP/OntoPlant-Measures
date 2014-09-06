**TODO**

07/03/14

- 3 "viste" sui dati per ciascun esempio; esplicitare cosa si colloca in ciascuna vista
- distinguere il LabOperator (può eseguire sia il Sampling che la SampleObservation, ma USA
un sensore - non è necessariamente "lui stesso" il sensore); la problematica di descrivere
l'osservazione attraverso un sensore effettuata dal LabOperator è "insita" nell'osservazione
nel laboratorio, pertanto non viene analizzata in questo momento
- modellare il sensore in Sensor-NoSample e l'esperto di lab. in Lab-Sample

**Change Log**

07/03/14

- Sampling (raccoglimento "fisico" del campione) != SampleObservation (analisi del campione)
- possibile inferire che, se un sample è collectioned in un collection point, una observation
fatta sul sample è fatta su quel collectionpoint
- aggiunto Sample e proprietà Sample.sampleOf : FeatureOfInterest
- plantObservation hasConstituent phObservation vs plantSensorOutput hasConstituent phSensorOutput
si tiene la prima versione perché in questo modo dalle singole observation è possibile ottenere
l'indicazione temporale, che attualmente non è prevista dal sensor output
- possibile inferire il "constituent" dei SensorOutput da quelli di Observatione e viceversa
[attualmente scelto di asserire hasConstituent di Observation]
...
- possibile inferire il refersToService di un SensorOutput attraverso il sensore (e viceversa)
[attualmente scelto di asserire direttamente refersToService]
...