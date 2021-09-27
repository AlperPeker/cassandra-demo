# Gerekli Komutlar

#### cassandra.repo dosyası oluşturduktan sonra Cassandra'yı yüklemek için:
> - yum install cassandra

#### Cassandra'yı bir servis olarak ayağa kaldırmak/durdurmak/durumunu öğrenmek için:
> - service cassandra start
> - service cassandra stop
> - service cassandra status

#### Yapılandırma değişiklikleri sonrasında data klasörünü temizlemek için:
> - rm -rf /var/lib/cassandra/data/system/*

#### Cassandra ayakta iken nodeların durumunu kontrol etmek için:
> - nodetool status
