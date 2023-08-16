# Postgres packaged for Immich Distribution

[Postgres](https://www.postgresql.org/) is a relationship database that I use in [Immich Distribution](https://github.com/nsg/immich-distribution). This repo is used as a dependency of the Immich Distribution project and is not intended for direct consumption.

## Usage

```yaml
stage-snaps:
    - immich-distribution-postgres/latest/stable
```

## Contents
```
.
├── meta
│   └── snap.yaml
└── usr
    └── local
        └── pgsql
            ├── bin
            │   ├── clusterdb
            │   ├── createdb
            │   ├── createuser
            │   ├── dropdb
            │   ├── dropuser
            │   ├── ecpg
            │   ├── initdb
            │   ├── oid2name
            │   ├── pg_amcheck
            │   ├── pg_archivecleanup
            │   ├── pg_basebackup
            │   ├── pgbench
            │   ├── pg_checksums
            │   ├── pg_config
            │   ├── pg_controldata
            │   ├── pg_ctl
            │   ├── pg_dump
            │   ├── pg_dumpall
            │   ├── pg_isready
            │   ├── pg_receivewal
            │   ├── pg_recvlogical
            │   ├── pg_resetwal
            │   ├── pg_restore
            │   ├── pg_rewind
            │   ├── pg_test_fsync
            │   ├── pg_test_timing
            │   ├── pg_upgrade
            │   ├── pg_verifybackup
            │   ├── pg_waldump
            │   ├── postgres
            │   ├── postmaster -> postgres
            │   ├── psql
            │   ├── reindexdb
            │   ├── vacuumdb
            │   └── vacuumlo
            ├── lib
            │   ├── adminpack.so
            │   ├── amcheck.so
            │   ├── auth_delay.so
            │   ├── auto_explain.so
            │   ├── autoinc.so
            │   ├── basebackup_to_shell.so
            │   ├── basic_archive.so
            │   ├── bloom.so
            │   ├── btree_gin.so
            │   ├── btree_gist.so
            │   ├── citext.so
            │   ├── cube.so
            │   ├── cyrillic_and_mic.so
            │   ├── dblink.so
            │   ├── dict_int.so
            │   ├── dict_snowball.so
            │   ├── dict_xsyn.so
            │   ├── earthdistance.so
            │   ├── euc2004_sjis2004.so
            │   ├── euc_cn_and_mic.so
            │   ├── euc_jp_and_sjis.so
            │   ├── euc_kr_and_mic.so
            │   ├── euc_tw_and_big5.so
            │   ├── file_fdw.so
            │   ├── fuzzystrmatch.so
            │   ├── hstore.so
            │   ├── insert_username.so
            │   ├── _int.so
            │   ├── isn.so
            │   ├── latin2_and_win1250.so
            │   ├── latin_and_mic.so
            │   ├── libecpg.a
            │   ├── libecpg_compat.a
            │   ├── libecpg_compat.so -> libecpg_compat.so.3.15
            │   ├── libecpg_compat.so.3 -> libecpg_compat.so.3.15
            │   ├── libecpg_compat.so.3.15
            │   ├── libecpg.so -> libecpg.so.6.15
            │   ├── libecpg.so.6 -> libecpg.so.6.15
            │   ├── libecpg.so.6.15
            │   ├── libpgcommon.a
            │   ├── libpgcommon_shlib.a
            │   ├── libpgfeutils.a
            │   ├── libpgport.a
            │   ├── libpgport_shlib.a
            │   ├── libpgtypes.a
            │   ├── libpgtypes.so -> libpgtypes.so.3.15
            │   ├── libpgtypes.so.3 -> libpgtypes.so.3.15
            │   ├── libpgtypes.so.3.15
            │   ├── libpq.a
            │   ├── libpq.so -> libpq.so.5.15
            │   ├── libpq.so.5 -> libpq.so.5.15
            │   ├── libpq.so.5.15
            │   ├── libpqwalreceiver.so
            │   ├── lo.so
            │   ├── ltree.so
            │   ├── moddatetime.so
            │   ├── old_snapshot.so
            │   ├── pageinspect.so
            │   ├── passwordcheck.so
            │   ├── pg_buffercache.so
            │   ├── pg_freespacemap.so
            │   ├── pgoutput.so
            │   ├── pg_prewarm.so
            │   ├── pgrowlocks.so
            │   ├── pg_stat_statements.so
            │   ├── pgstattuple.so
            │   ├── pg_surgery.so
            │   ├── pg_trgm.so
            │   ├── pg_visibility.so
            │   ├── pg_walinspect.so
            │   ├── pgxs
            │   │   ├── config
            │   │   │   ├── install-sh
            │   │   │   └── missing
            │   │   └── src
            │   │       ├── Makefile.global
            │   │       ├── Makefile.port
            │   │       ├── makefiles
            │   │       │   └── pgxs.mk
            │   │       ├── Makefile.shlib
            │   │       ├── nls-global.mk
            │   │       └── test
            │   │           ├── isolation
            │   │           │   ├── isolationtester
            │   │           │   └── pg_isolation_regress
            │   │           └── regress
            │   │               └── pg_regress
            │   ├── pkgconfig
            │   │   ├── libecpg_compat.pc
            │   │   ├── libecpg.pc
            │   │   ├── libpgtypes.pc
            │   │   └── libpq.pc
            │   ├── plpgsql.so
            │   ├── postgres_fdw.so
            │   ├── refint.so
            │   ├── seg.so
            │   ├── tablefunc.so
            │   ├── tcn.so
            │   ├── test_decoding.so
            │   ├── tsm_system_rows.so
            │   ├── tsm_system_time.so
            │   ├── unaccent.so
            │   ├── utf8_and_big5.so
            │   ├── utf8_and_cyrillic.so
            │   ├── utf8_and_euc2004.so
            │   ├── utf8_and_euc_cn.so
            │   ├── utf8_and_euc_jp.so
            │   ├── utf8_and_euc_kr.so
            │   ├── utf8_and_euc_tw.so
            │   ├── utf8_and_gb18030.so
            │   ├── utf8_and_gbk.so
            │   ├── utf8_and_iso8859_1.so
            │   ├── utf8_and_iso8859.so
            │   ├── utf8_and_johab.so
            │   ├── utf8_and_sjis2004.so
            │   ├── utf8_and_sjis.so
            │   ├── utf8_and_uhc.so
            │   ├── utf8_and_win.so
            │   └── uuid-ossp.so
            └── share
                ├── doc
                │   └── extension
                │       ├── autoinc.example
                │       ├── insert_username.example
                │       ├── moddatetime.example
                │       └── refint.example
                ├── errcodes.txt
                ├── extension
                │   ├── adminpack--1.0--1.1.sql
                │   ├── adminpack--1.0.sql
                │   ├── adminpack--1.1--2.0.sql
                │   ├── adminpack--2.0--2.1.sql
                │   ├── adminpack.control
                │   ├── amcheck--1.0--1.1.sql
                │   ├── amcheck--1.0.sql
                │   ├── amcheck--1.1--1.2.sql
                │   ├── amcheck--1.2--1.3.sql
                │   ├── amcheck.control
                │   ├── autoinc--1.0.sql
                │   ├── autoinc.control
                │   ├── bloom--1.0.sql
                │   ├── bloom.control
                │   ├── btree_gin--1.0--1.1.sql
                │   ├── btree_gin--1.0.sql
                │   ├── btree_gin--1.1--1.2.sql
                │   ├── btree_gin--1.2--1.3.sql
                │   ├── btree_gin.control
                │   ├── btree_gist--1.0--1.1.sql
                │   ├── btree_gist--1.1--1.2.sql
                │   ├── btree_gist--1.2--1.3.sql
                │   ├── btree_gist--1.2.sql
                │   ├── btree_gist--1.3--1.4.sql
                │   ├── btree_gist--1.4--1.5.sql
                │   ├── btree_gist--1.5--1.6.sql
                │   ├── btree_gist--1.6--1.7.sql
                │   ├── btree_gist.control
                │   ├── citext--1.0--1.1.sql
                │   ├── citext--1.1--1.2.sql
                │   ├── citext--1.2--1.3.sql
                │   ├── citext--1.3--1.4.sql
                │   ├── citext--1.4--1.5.sql
                │   ├── citext--1.4.sql
                │   ├── citext--1.5--1.6.sql
                │   ├── citext.control
                │   ├── cube--1.0--1.1.sql
                │   ├── cube--1.1--1.2.sql
                │   ├── cube--1.2--1.3.sql
                │   ├── cube--1.2.sql
                │   ├── cube--1.3--1.4.sql
                │   ├── cube--1.4--1.5.sql
                │   ├── cube.control
                │   ├── dblink--1.0--1.1.sql
                │   ├── dblink--1.1--1.2.sql
                │   ├── dblink--1.2.sql
                │   ├── dblink.control
                │   ├── dict_int--1.0.sql
                │   ├── dict_int.control
                │   ├── dict_xsyn--1.0.sql
                │   ├── dict_xsyn.control
                │   ├── earthdistance--1.0--1.1.sql
                │   ├── earthdistance--1.1.sql
                │   ├── earthdistance.control
                │   ├── file_fdw--1.0.sql
                │   ├── file_fdw.control
                │   ├── fuzzystrmatch--1.0--1.1.sql
                │   ├── fuzzystrmatch--1.1.sql
                │   ├── fuzzystrmatch.control
                │   ├── hstore--1.1--1.2.sql
                │   ├── hstore--1.2--1.3.sql
                │   ├── hstore--1.3--1.4.sql
                │   ├── hstore--1.4--1.5.sql
                │   ├── hstore--1.4.sql
                │   ├── hstore--1.5--1.6.sql
                │   ├── hstore--1.6--1.7.sql
                │   ├── hstore--1.7--1.8.sql
                │   ├── hstore.control
                │   ├── insert_username--1.0.sql
                │   ├── insert_username.control
                │   ├── intagg--1.0--1.1.sql
                │   ├── intagg--1.1.sql
                │   ├── intagg.control
                │   ├── intarray--1.0--1.1.sql
                │   ├── intarray--1.1--1.2.sql
                │   ├── intarray--1.2--1.3.sql
                │   ├── intarray--1.2.sql
                │   ├── intarray--1.3--1.4.sql
                │   ├── intarray--1.4--1.5.sql
                │   ├── intarray.control
                │   ├── isn--1.0--1.1.sql
                │   ├── isn--1.1--1.2.sql
                │   ├── isn--1.1.sql
                │   ├── isn.control
                │   ├── lo--1.0--1.1.sql
                │   ├── lo--1.1.sql
                │   ├── lo.control
                │   ├── ltree--1.0--1.1.sql
                │   ├── ltree--1.1--1.2.sql
                │   ├── ltree--1.1.sql
                │   ├── ltree.control
                │   ├── moddatetime--1.0.sql
                │   ├── moddatetime.control
                │   ├── old_snapshot--1.0.sql
                │   ├── old_snapshot.control
                │   ├── pageinspect--1.0--1.1.sql
                │   ├── pageinspect--1.10--1.11.sql
                │   ├── pageinspect--1.1--1.2.sql
                │   ├── pageinspect--1.2--1.3.sql
                │   ├── pageinspect--1.3--1.4.sql
                │   ├── pageinspect--1.4--1.5.sql
                │   ├── pageinspect--1.5--1.6.sql
                │   ├── pageinspect--1.5.sql
                │   ├── pageinspect--1.6--1.7.sql
                │   ├── pageinspect--1.7--1.8.sql
                │   ├── pageinspect--1.8--1.9.sql
                │   ├── pageinspect--1.9--1.10.sql
                │   ├── pageinspect.control
                │   ├── pg_buffercache--1.0--1.1.sql
                │   ├── pg_buffercache--1.1--1.2.sql
                │   ├── pg_buffercache--1.2--1.3.sql
                │   ├── pg_buffercache--1.2.sql
                │   ├── pg_buffercache.control
                │   ├── pg_freespacemap--1.0--1.1.sql
                │   ├── pg_freespacemap--1.1--1.2.sql
                │   ├── pg_freespacemap--1.1.sql
                │   ├── pg_freespacemap.control
                │   ├── pg_prewarm--1.0--1.1.sql
                │   ├── pg_prewarm--1.1--1.2.sql
                │   ├── pg_prewarm--1.1.sql
                │   ├── pg_prewarm.control
                │   ├── pgrowlocks--1.0--1.1.sql
                │   ├── pgrowlocks--1.1--1.2.sql
                │   ├── pgrowlocks--1.2.sql
                │   ├── pgrowlocks.control
                │   ├── pg_stat_statements--1.0--1.1.sql
                │   ├── pg_stat_statements--1.1--1.2.sql
                │   ├── pg_stat_statements--1.2--1.3.sql
                │   ├── pg_stat_statements--1.3--1.4.sql
                │   ├── pg_stat_statements--1.4--1.5.sql
                │   ├── pg_stat_statements--1.4.sql
                │   ├── pg_stat_statements--1.5--1.6.sql
                │   ├── pg_stat_statements--1.6--1.7.sql
                │   ├── pg_stat_statements--1.7--1.8.sql
                │   ├── pg_stat_statements--1.8--1.9.sql
                │   ├── pg_stat_statements--1.9--1.10.sql
                │   ├── pg_stat_statements.control
                │   ├── pgstattuple--1.0--1.1.sql
                │   ├── pgstattuple--1.1--1.2.sql
                │   ├── pgstattuple--1.2--1.3.sql
                │   ├── pgstattuple--1.3--1.4.sql
                │   ├── pgstattuple--1.4--1.5.sql
                │   ├── pgstattuple--1.4.sql
                │   ├── pgstattuple.control
                │   ├── pg_surgery--1.0.sql
                │   ├── pg_surgery.control
                │   ├── pg_trgm--1.0--1.1.sql
                │   ├── pg_trgm--1.1--1.2.sql
                │   ├── pg_trgm--1.2--1.3.sql
                │   ├── pg_trgm--1.3--1.4.sql
                │   ├── pg_trgm--1.3.sql
                │   ├── pg_trgm--1.4--1.5.sql
                │   ├── pg_trgm--1.5--1.6.sql
                │   ├── pg_trgm.control
                │   ├── pg_visibility--1.0--1.1.sql
                │   ├── pg_visibility--1.1--1.2.sql
                │   ├── pg_visibility--1.1.sql
                │   ├── pg_visibility.control
                │   ├── pg_walinspect--1.0.sql
                │   ├── pg_walinspect.control
                │   ├── plpgsql--1.0.sql
                │   ├── plpgsql.control
                │   ├── postgres_fdw--1.0--1.1.sql
                │   ├── postgres_fdw--1.0.sql
                │   ├── postgres_fdw.control
                │   ├── refint--1.0.sql
                │   ├── refint.control
                │   ├── seg--1.0--1.1.sql
                │   ├── seg--1.1--1.2.sql
                │   ├── seg--1.1.sql
                │   ├── seg--1.2--1.3.sql
                │   ├── seg--1.3--1.4.sql
                │   ├── seg.control
                │   ├── tablefunc--1.0.sql
                │   ├── tablefunc.control
                │   ├── tcn--1.0.sql
                │   ├── tcn.control
                │   ├── tsm_system_rows--1.0.sql
                │   ├── tsm_system_rows.control
                │   ├── tsm_system_time--1.0.sql
                │   ├── tsm_system_time.control
                │   ├── unaccent--1.0--1.1.sql
                │   ├── unaccent--1.1.sql
                │   ├── unaccent.control
                │   ├── uuid-ossp--1.0--1.1.sql
                │   ├── uuid-ossp--1.1.sql
                │   └── uuid-ossp.control
                ├── information_schema.sql
                ├── pg_hba.conf.sample
                ├── pg_ident.conf.sample
                ├── pg_service.conf.sample
                ├── postgres.bki
                ├── postgresql.conf.sample
                ├── psqlrc.sample
                ├── snowball_create.sql
                ├── sql_features.txt
                ├── system_constraints.sql
                ├── system_functions.sql
                ├── system_views.sql
                ├── timezone
                │   ├── Africa
                │   │   ├── Abidjan
                │   │   ├── Accra
                │   │   ├── Addis_Ababa
                │   │   ├── Algiers
                │   │   ├── Asmara
                │   │   ├── Asmera
                │   │   ├── Bamako
                │   │   ├── Bangui
                │   │   ├── Banjul
                │   │   ├── Bissau
                │   │   ├── Blantyre
                │   │   ├── Brazzaville
                │   │   ├── Bujumbura
                │   │   ├── Cairo
                │   │   ├── Casablanca
                │   │   ├── Ceuta
                │   │   ├── Conakry
                │   │   ├── Dakar
                │   │   ├── Dar_es_Salaam
                │   │   ├── Djibouti
                │   │   ├── Douala
                │   │   ├── El_Aaiun
                │   │   ├── Freetown
                │   │   ├── Gaborone
                │   │   ├── Harare
                │   │   ├── Johannesburg
                │   │   ├── Juba
                │   │   ├── Kampala
                │   │   ├── Khartoum
                │   │   ├── Kigali
                │   │   ├── Kinshasa
                │   │   ├── Lagos
                │   │   ├── Libreville
                │   │   ├── Lome
                │   │   ├── Luanda
                │   │   ├── Lubumbashi
                │   │   ├── Lusaka
                │   │   ├── Malabo
                │   │   ├── Maputo
                │   │   ├── Maseru
                │   │   ├── Mbabane
                │   │   ├── Mogadishu
                │   │   ├── Monrovia
                │   │   ├── Nairobi
                │   │   ├── Ndjamena
                │   │   ├── Niamey
                │   │   ├── Nouakchott
                │   │   ├── Ouagadougou
                │   │   ├── Porto-Novo
                │   │   ├── Sao_Tome
                │   │   ├── Timbuktu
                │   │   ├── Tripoli
                │   │   ├── Tunis
                │   │   └── Windhoek
                │   ├── America
                │   │   ├── Adak
                │   │   ├── Anchorage
                │   │   ├── Anguilla
                │   │   ├── Antigua
                │   │   ├── Araguaina
                │   │   ├── Argentina
                │   │   │   ├── Buenos_Aires
                │   │   │   ├── Catamarca
                │   │   │   ├── ComodRivadavia
                │   │   │   ├── Cordoba
                │   │   │   ├── Jujuy
                │   │   │   ├── La_Rioja
                │   │   │   ├── Mendoza
                │   │   │   ├── Rio_Gallegos
                │   │   │   ├── Salta
                │   │   │   ├── San_Juan
                │   │   │   ├── San_Luis
                │   │   │   ├── Tucuman
                │   │   │   └── Ushuaia
                │   │   ├── Aruba
                │   │   ├── Asuncion
                │   │   ├── Atikokan
                │   │   ├── Atka
                │   │   ├── Bahia
                │   │   ├── Bahia_Banderas
                │   │   ├── Barbados
                │   │   ├── Belem
                │   │   ├── Belize
                │   │   ├── Blanc-Sablon
                │   │   ├── Boa_Vista
                │   │   ├── Bogota
                │   │   ├── Boise
                │   │   ├── Buenos_Aires
                │   │   ├── Cambridge_Bay
                │   │   ├── Campo_Grande
                │   │   ├── Cancun
                │   │   ├── Caracas
                │   │   ├── Catamarca
                │   │   ├── Cayenne
                │   │   ├── Cayman
                │   │   ├── Chicago
                │   │   ├── Chihuahua
                │   │   ├── Ciudad_Juarez
                │   │   ├── Coral_Harbour
                │   │   ├── Cordoba
                │   │   ├── Costa_Rica
                │   │   ├── Creston
                │   │   ├── Cuiaba
                │   │   ├── Curacao
                │   │   ├── Danmarkshavn
                │   │   ├── Dawson
                │   │   ├── Dawson_Creek
                │   │   ├── Denver
                │   │   ├── Detroit
                │   │   ├── Dominica
                │   │   ├── Edmonton
                │   │   ├── Eirunepe
                │   │   ├── El_Salvador
                │   │   ├── Ensenada
                │   │   ├── Fortaleza
                │   │   ├── Fort_Nelson
                │   │   ├── Fort_Wayne
                │   │   ├── Glace_Bay
                │   │   ├── Godthab
                │   │   ├── Goose_Bay
                │   │   ├── Grand_Turk
                │   │   ├── Grenada
                │   │   ├── Guadeloupe
                │   │   ├── Guatemala
                │   │   ├── Guayaquil
                │   │   ├── Guyana
                │   │   ├── Halifax
                │   │   ├── Havana
                │   │   ├── Hermosillo
                │   │   ├── Indiana
                │   │   │   ├── Indianapolis
                │   │   │   ├── Knox
                │   │   │   ├── Marengo
                │   │   │   ├── Petersburg
                │   │   │   ├── Tell_City
                │   │   │   ├── Vevay
                │   │   │   ├── Vincennes
                │   │   │   └── Winamac
                │   │   ├── Indianapolis
                │   │   ├── Inuvik
                │   │   ├── Iqaluit
                │   │   ├── Jamaica
                │   │   ├── Jujuy
                │   │   ├── Juneau
                │   │   ├── Kentucky
                │   │   │   ├── Louisville
                │   │   │   └── Monticello
                │   │   ├── Knox_IN
                │   │   ├── Kralendijk
                │   │   ├── La_Paz
                │   │   ├── Lima
                │   │   ├── Los_Angeles
                │   │   ├── Louisville
                │   │   ├── Lower_Princes
                │   │   ├── Maceio
                │   │   ├── Managua
                │   │   ├── Manaus
                │   │   ├── Marigot
                │   │   ├── Martinique
                │   │   ├── Matamoros
                │   │   ├── Mazatlan
                │   │   ├── Mendoza
                │   │   ├── Menominee
                │   │   ├── Merida
                │   │   ├── Metlakatla
                │   │   ├── Mexico_City
                │   │   ├── Miquelon
                │   │   ├── Moncton
                │   │   ├── Monterrey
                │   │   ├── Montevideo
                │   │   ├── Montreal
                │   │   ├── Montserrat
                │   │   ├── Nassau
                │   │   ├── New_York
                │   │   ├── Nipigon
                │   │   ├── Nome
                │   │   ├── Noronha
                │   │   ├── North_Dakota
                │   │   │   ├── Beulah
                │   │   │   ├── Center
                │   │   │   └── New_Salem
                │   │   ├── Nuuk
                │   │   ├── Ojinaga
                │   │   ├── Panama
                │   │   ├── Pangnirtung
                │   │   ├── Paramaribo
                │   │   ├── Phoenix
                │   │   ├── Port-au-Prince
                │   │   ├── Porto_Acre
                │   │   ├── Port_of_Spain
                │   │   ├── Porto_Velho
                │   │   ├── Puerto_Rico
                │   │   ├── Punta_Arenas
                │   │   ├── Rainy_River
                │   │   ├── Rankin_Inlet
                │   │   ├── Recife
                │   │   ├── Regina
                │   │   ├── Resolute
                │   │   ├── Rio_Branco
                │   │   ├── Rosario
                │   │   ├── Santa_Isabel
                │   │   ├── Santarem
                │   │   ├── Santiago
                │   │   ├── Santo_Domingo
                │   │   ├── Sao_Paulo
                │   │   ├── Scoresbysund
                │   │   ├── Shiprock
                │   │   ├── Sitka
                │   │   ├── St_Barthelemy
                │   │   ├── St_Johns
                │   │   ├── St_Kitts
                │   │   ├── St_Lucia
                │   │   ├── St_Thomas
                │   │   ├── St_Vincent
                │   │   ├── Swift_Current
                │   │   ├── Tegucigalpa
                │   │   ├── Thule
                │   │   ├── Thunder_Bay
                │   │   ├── Tijuana
                │   │   ├── Toronto
                │   │   ├── Tortola
                │   │   ├── Vancouver
                │   │   ├── Virgin
                │   │   ├── Whitehorse
                │   │   ├── Winnipeg
                │   │   ├── Yakutat
                │   │   └── Yellowknife
                │   ├── Antarctica
                │   │   ├── Casey
                │   │   ├── Davis
                │   │   ├── DumontDUrville
                │   │   ├── Macquarie
                │   │   ├── Mawson
                │   │   ├── McMurdo
                │   │   ├── Palmer
                │   │   ├── Rothera
                │   │   ├── South_Pole
                │   │   ├── Syowa
                │   │   ├── Troll
                │   │   └── Vostok
                │   ├── Arctic
                │   │   └── Longyearbyen
                │   ├── Asia
                │   │   ├── Aden
                │   │   ├── Almaty
                │   │   ├── Amman
                │   │   ├── Anadyr
                │   │   ├── Aqtau
                │   │   ├── Aqtobe
                │   │   ├── Ashgabat
                │   │   ├── Ashkhabad
                │   │   ├── Atyrau
                │   │   ├── Baghdad
                │   │   ├── Bahrain
                │   │   ├── Baku
                │   │   ├── Bangkok
                │   │   ├── Barnaul
                │   │   ├── Beirut
                │   │   ├── Bishkek
                │   │   ├── Brunei
                │   │   ├── Calcutta
                │   │   ├── Chita
                │   │   ├── Choibalsan
                │   │   ├── Chongqing
                │   │   ├── Chungking
                │   │   ├── Colombo
                │   │   ├── Dacca
                │   │   ├── Damascus
                │   │   ├── Dhaka
                │   │   ├── Dili
                │   │   ├── Dubai
                │   │   ├── Dushanbe
                │   │   ├── Famagusta
                │   │   ├── Gaza
                │   │   ├── Harbin
                │   │   ├── Hebron
                │   │   ├── Ho_Chi_Minh
                │   │   ├── Hong_Kong
                │   │   ├── Hovd
                │   │   ├── Irkutsk
                │   │   ├── Istanbul
                │   │   ├── Jakarta
                │   │   ├── Jayapura
                │   │   ├── Jerusalem
                │   │   ├── Kabul
                │   │   ├── Kamchatka
                │   │   ├── Karachi
                │   │   ├── Kashgar
                │   │   ├── Kathmandu
                │   │   ├── Katmandu
                │   │   ├── Khandyga
                │   │   ├── Kolkata
                │   │   ├── Krasnoyarsk
                │   │   ├── Kuala_Lumpur
                │   │   ├── Kuching
                │   │   ├── Kuwait
                │   │   ├── Macao
                │   │   ├── Macau
                │   │   ├── Magadan
                │   │   ├── Makassar
                │   │   ├── Manila
                │   │   ├── Muscat
                │   │   ├── Nicosia
                │   │   ├── Novokuznetsk
                │   │   ├── Novosibirsk
                │   │   ├── Omsk
                │   │   ├── Oral
                │   │   ├── Phnom_Penh
                │   │   ├── Pontianak
                │   │   ├── Pyongyang
                │   │   ├── Qatar
                │   │   ├── Qostanay
                │   │   ├── Qyzylorda
                │   │   ├── Rangoon
                │   │   ├── Riyadh
                │   │   ├── Saigon
                │   │   ├── Sakhalin
                │   │   ├── Samarkand
                │   │   ├── Seoul
                │   │   ├── Shanghai
                │   │   ├── Singapore
                │   │   ├── Srednekolymsk
                │   │   ├── Taipei
                │   │   ├── Tashkent
                │   │   ├── Tbilisi
                │   │   ├── Tehran
                │   │   ├── Tel_Aviv
                │   │   ├── Thimbu
                │   │   ├── Thimphu
                │   │   ├── Tokyo
                │   │   ├── Tomsk
                │   │   ├── Ujung_Pandang
                │   │   ├── Ulaanbaatar
                │   │   ├── Ulan_Bator
                │   │   ├── Urumqi
                │   │   ├── Ust-Nera
                │   │   ├── Vientiane
                │   │   ├── Vladivostok
                │   │   ├── Yakutsk
                │   │   ├── Yangon
                │   │   ├── Yekaterinburg
                │   │   └── Yerevan
                │   ├── Atlantic
                │   │   ├── Azores
                │   │   ├── Bermuda
                │   │   ├── Canary
                │   │   ├── Cape_Verde
                │   │   ├── Faeroe
                │   │   ├── Faroe
                │   │   ├── Jan_Mayen
                │   │   ├── Madeira
                │   │   ├── Reykjavik
                │   │   ├── South_Georgia
                │   │   ├── Stanley
                │   │   └── St_Helena
                │   ├── Australia
                │   │   ├── ACT
                │   │   ├── Adelaide
                │   │   ├── Brisbane
                │   │   ├── Broken_Hill
                │   │   ├── Canberra
                │   │   ├── Currie
                │   │   ├── Darwin
                │   │   ├── Eucla
                │   │   ├── Hobart
                │   │   ├── LHI
                │   │   ├── Lindeman
                │   │   ├── Lord_Howe
                │   │   ├── Melbourne
                │   │   ├── North
                │   │   ├── NSW
                │   │   ├── Perth
                │   │   ├── Queensland
                │   │   ├── South
                │   │   ├── Sydney
                │   │   ├── Tasmania
                │   │   ├── Victoria
                │   │   ├── West
                │   │   └── Yancowinna
                │   ├── Brazil
                │   │   ├── Acre
                │   │   ├── DeNoronha
                │   │   ├── East
                │   │   └── West
                │   ├── Canada
                │   │   ├── Atlantic
                │   │   ├── Central
                │   │   ├── Eastern
                │   │   ├── Mountain
                │   │   ├── Newfoundland
                │   │   ├── Pacific
                │   │   ├── Saskatchewan
                │   │   └── Yukon
                │   ├── CET
                │   ├── Chile
                │   │   ├── Continental
                │   │   └── EasterIsland
                │   ├── CST6CDT
                │   ├── Cuba
                │   ├── EET
                │   ├── Egypt
                │   ├── Eire
                │   ├── EST
                │   ├── EST5EDT
                │   ├── Etc
                │   │   ├── GMT
                │   │   ├── GMT+0
                │   │   ├── GMT-0
                │   │   ├── GMT0
                │   │   ├── GMT+1
                │   │   ├── GMT-1
                │   │   ├── GMT+10
                │   │   ├── GMT-10
                │   │   ├── GMT+11
                │   │   ├── GMT-11
                │   │   ├── GMT+12
                │   │   ├── GMT-12
                │   │   ├── GMT-13
                │   │   ├── GMT-14
                │   │   ├── GMT+2
                │   │   ├── GMT-2
                │   │   ├── GMT+3
                │   │   ├── GMT-3
                │   │   ├── GMT+4
                │   │   ├── GMT-4
                │   │   ├── GMT+5
                │   │   ├── GMT-5
                │   │   ├── GMT+6
                │   │   ├── GMT-6
                │   │   ├── GMT+7
                │   │   ├── GMT-7
                │   │   ├── GMT+8
                │   │   ├── GMT-8
                │   │   ├── GMT+9
                │   │   ├── GMT-9
                │   │   ├── Greenwich
                │   │   ├── UCT
                │   │   ├── Universal
                │   │   ├── UTC
                │   │   └── Zulu
                │   ├── Europe
                │   │   ├── Amsterdam
                │   │   ├── Andorra
                │   │   ├── Astrakhan
                │   │   ├── Athens
                │   │   ├── Belfast
                │   │   ├── Belgrade
                │   │   ├── Berlin
                │   │   ├── Bratislava
                │   │   ├── Brussels
                │   │   ├── Bucharest
                │   │   ├── Budapest
                │   │   ├── Busingen
                │   │   ├── Chisinau
                │   │   ├── Copenhagen
                │   │   ├── Dublin
                │   │   ├── Gibraltar
                │   │   ├── Guernsey
                │   │   ├── Helsinki
                │   │   ├── Isle_of_Man
                │   │   ├── Istanbul
                │   │   ├── Jersey
                │   │   ├── Kaliningrad
                │   │   ├── Kiev
                │   │   ├── Kirov
                │   │   ├── Kyiv
                │   │   ├── Lisbon
                │   │   ├── Ljubljana
                │   │   ├── London
                │   │   ├── Luxembourg
                │   │   ├── Madrid
                │   │   ├── Malta
                │   │   ├── Mariehamn
                │   │   ├── Minsk
                │   │   ├── Monaco
                │   │   ├── Moscow
                │   │   ├── Nicosia
                │   │   ├── Oslo
                │   │   ├── Paris
                │   │   ├── Podgorica
                │   │   ├── Prague
                │   │   ├── Riga
                │   │   ├── Rome
                │   │   ├── Samara
                │   │   ├── San_Marino
                │   │   ├── Sarajevo
                │   │   ├── Saratov
                │   │   ├── Simferopol
                │   │   ├── Skopje
                │   │   ├── Sofia
                │   │   ├── Stockholm
                │   │   ├── Tallinn
                │   │   ├── Tirane
                │   │   ├── Tiraspol
                │   │   ├── Ulyanovsk
                │   │   ├── Uzhgorod
                │   │   ├── Vaduz
                │   │   ├── Vatican
                │   │   ├── Vienna
                │   │   ├── Vilnius
                │   │   ├── Volgograd
                │   │   ├── Warsaw
                │   │   ├── Zagreb
                │   │   ├── Zaporozhye
                │   │   └── Zurich
                │   ├── Factory
                │   ├── GB
                │   ├── GB-Eire
                │   ├── GMT
                │   ├── GMT+0
                │   ├── GMT-0
                │   ├── GMT0
                │   ├── Greenwich
                │   ├── Hongkong
                │   ├── HST
                │   ├── Iceland
                │   ├── Indian
                │   │   ├── Antananarivo
                │   │   ├── Chagos
                │   │   ├── Christmas
                │   │   ├── Cocos
                │   │   ├── Comoro
                │   │   ├── Kerguelen
                │   │   ├── Mahe
                │   │   ├── Maldives
                │   │   ├── Mauritius
                │   │   ├── Mayotte
                │   │   └── Reunion
                │   ├── Iran
                │   ├── Israel
                │   ├── Jamaica
                │   ├── Japan
                │   ├── Kwajalein
                │   ├── Libya
                │   ├── MET
                │   ├── Mexico
                │   │   ├── BajaNorte
                │   │   ├── BajaSur
                │   │   └── General
                │   ├── MST
                │   ├── MST7MDT
                │   ├── Navajo
                │   ├── NZ
                │   ├── NZ-CHAT
                │   ├── Pacific
                │   │   ├── Apia
                │   │   ├── Auckland
                │   │   ├── Bougainville
                │   │   ├── Chatham
                │   │   ├── Chuuk
                │   │   ├── Easter
                │   │   ├── Efate
                │   │   ├── Enderbury
                │   │   ├── Fakaofo
                │   │   ├── Fiji
                │   │   ├── Funafuti
                │   │   ├── Galapagos
                │   │   ├── Gambier
                │   │   ├── Guadalcanal
                │   │   ├── Guam
                │   │   ├── Honolulu
                │   │   ├── Johnston
                │   │   ├── Kanton
                │   │   ├── Kiritimati
                │   │   ├── Kosrae
                │   │   ├── Kwajalein
                │   │   ├── Majuro
                │   │   ├── Marquesas
                │   │   ├── Midway
                │   │   ├── Nauru
                │   │   ├── Niue
                │   │   ├── Norfolk
                │   │   ├── Noumea
                │   │   ├── Pago_Pago
                │   │   ├── Palau
                │   │   ├── Pitcairn
                │   │   ├── Pohnpei
                │   │   ├── Ponape
                │   │   ├── Port_Moresby
                │   │   ├── Rarotonga
                │   │   ├── Saipan
                │   │   ├── Samoa
                │   │   ├── Tahiti
                │   │   ├── Tarawa
                │   │   ├── Tongatapu
                │   │   ├── Truk
                │   │   ├── Wake
                │   │   ├── Wallis
                │   │   └── Yap
                │   ├── Poland
                │   ├── Portugal
                │   ├── PRC
                │   ├── PST8PDT
                │   ├── ROC
                │   ├── ROK
                │   ├── Singapore
                │   ├── Turkey
                │   ├── UCT
                │   ├── Universal
                │   ├── US
                │   │   ├── Alaska
                │   │   ├── Aleutian
                │   │   ├── Arizona
                │   │   ├── Central
                │   │   ├── Eastern
                │   │   ├── East-Indiana
                │   │   ├── Hawaii
                │   │   ├── Indiana-Starke
                │   │   ├── Michigan
                │   │   ├── Mountain
                │   │   ├── Pacific
                │   │   └── Samoa
                │   ├── UTC
                │   ├── WET
                │   ├── W-SU
                │   └── Zulu
                ├── timezonesets
                │   ├── Africa.txt
                │   ├── America.txt
                │   ├── Antarctica.txt
                │   ├── Asia.txt
                │   ├── Atlantic.txt
                │   ├── Australia
                │   ├── Australia.txt
                │   ├── Default
                │   ├── Etc.txt
                │   ├── Europe.txt
                │   ├── India
                │   ├── Indian.txt
                │   └── Pacific.txt
                └── tsearch_data
                    ├── danish.stop
                    ├── dutch.stop
                    ├── english.stop
                    ├── finnish.stop
                    ├── french.stop
                    ├── german.stop
                    ├── hungarian.stop
                    ├── hunspell_sample.affix
                    ├── hunspell_sample_long.affix
                    ├── hunspell_sample_long.dict
                    ├── hunspell_sample_num.affix
                    ├── hunspell_sample_num.dict
                    ├── ispell_sample.affix
                    ├── ispell_sample.dict
                    ├── italian.stop
                    ├── nepali.stop
                    ├── norwegian.stop
                    ├── portuguese.stop
                    ├── russian.stop
                    ├── spanish.stop
                    ├── swedish.stop
                    ├── synonym_sample.syn
                    ├── thesaurus_sample.ths
                    ├── turkish.stop
                    ├── unaccent.rules
                    └── xsyn_sample.rules
```
