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

#### Örnek cqlsh komutları
> - REATE KEYSPACE demo WITH REPLICATION = {'class': SimpleStrategy, 'replication_factor': 3};
> - ALTER KEYSPACE demo WITH REPLICATION = {'class': 'SimpleStrategy', 'replication_factor': 1};
> - CREATE TABLE demo.kullanicilar (id uuid, name varchar, l_name varchar, b_date date, PRIMARY KEY (id));
> - INSERT INTO demo.kullanicilar (id, name, l_name, b_date) VALUES (uuid(), 'Albert', 'Parker', '1998-10-01');
> - SELECT * FROM demo.kullanicilar;
> - cqlsh -f ornekdata.cql  -> dışarıdan bir dosyayla data eklemek için
> - DELETE FROM demo.kullanicilar WHERE id = 84fb233f-6021-4e4b-aaba-097ab8dcea02;
> - DROP TABLE demo.kullanicilar;
> - DROP KEYSPACE IF EXISTS demo;
