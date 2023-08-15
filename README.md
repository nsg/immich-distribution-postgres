# Postgres packaged for Immich Distribution

[Postgres](https://www.postgresql.org/) is a relationship database that I use in [Immich Distribution](https://github.com/nsg/immich-distribution). This repo is used as a dependency of the Immich Distribution project and is not intended for direct consumption.

## Usage

```yaml
stage-snaps:
    - immich-distribution-postgres/latest/stable
```

## Contents

TODO: clean up

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
            ├── include
            │   ├── ecpg_config.h
            │   ├── ecpgerrno.h
            │   ├── ecpg_informix.h
            │   ├── ecpglib.h
            │   ├── ecpgtype.h
            │   ├── informix
            │   │   └── esql
            │   │       ├── datetime.h
            │   │       ├── decimal.h
            │   │       └── sqltypes.h
            │   ├── internal
            │   │   ├── c.h
            │   │   ├── fe-auth-sasl.h
            │   │   ├── libpq
            │   │   │   └── pqcomm.h
            │   │   ├── libpq-int.h
            │   │   ├── port.h
            │   │   ├── postgres_fe.h
            │   │   └── pqexpbuffer.h
            │   ├── libpq
            │   │   └── libpq-fs.h
            │   ├── libpq-events.h
            │   ├── libpq-fe.h
            │   ├── pg_config_ext.h
            │   ├── pg_config.h
            │   ├── pg_config_manual.h
            │   ├── pg_config_os.h
            │   ├── pgtypes_date.h
            │   ├── pgtypes_error.h
            │   ├── pgtypes.h
            │   ├── pgtypes_interval.h
            │   ├── pgtypes_numeric.h
            │   ├── pgtypes_timestamp.h
            │   ├── postgres_ext.h
            │   ├── server
            │   │   ├── access
            │   │   │   ├── amapi.h
            │   │   │   ├── amvalidate.h
            │   │   │   ├── attmap.h
            │   │   │   ├── attnum.h
            │   │   │   ├── brin.h
            │   │   │   ├── brin_internal.h
            │   │   │   ├── brin_page.h
            │   │   │   ├── brin_pageops.h
            │   │   │   ├── brin_revmap.h
            │   │   │   ├── brin_tuple.h
            │   │   │   ├── brin_xlog.h
            │   │   │   ├── bufmask.h
            │   │   │   ├── clog.h
            │   │   │   ├── commit_ts.h
            │   │   │   ├── detoast.h
            │   │   │   ├── genam.h
            │   │   │   ├── generic_xlog.h
            │   │   │   ├── ginblock.h
            │   │   │   ├── gin.h
            │   │   │   ├── gin_private.h
            │   │   │   ├── ginxlog.h
            │   │   │   ├── gist.h
            │   │   │   ├── gist_private.h
            │   │   │   ├── gistscan.h
            │   │   │   ├── gistxlog.h
            │   │   │   ├── hash.h
            │   │   │   ├── hash_xlog.h
            │   │   │   ├── heapam.h
            │   │   │   ├── heapam_xlog.h
            │   │   │   ├── heaptoast.h
            │   │   │   ├── hio.h
            │   │   │   ├── htup_details.h
            │   │   │   ├── htup.h
            │   │   │   ├── itup.h
            │   │   │   ├── multixact.h
            │   │   │   ├── nbtree.h
            │   │   │   ├── nbtxlog.h
            │   │   │   ├── parallel.h
            │   │   │   ├── printsimple.h
            │   │   │   ├── printtup.h
            │   │   │   ├── relation.h
            │   │   │   ├── reloptions.h
            │   │   │   ├── relscan.h
            │   │   │   ├── rewriteheap.h
            │   │   │   ├── rmgr.h
            │   │   │   ├── rmgrlist.h
            │   │   │   ├── sdir.h
            │   │   │   ├── session.h
            │   │   │   ├── skey.h
            │   │   │   ├── slru.h
            │   │   │   ├── spgist.h
            │   │   │   ├── spgist_private.h
            │   │   │   ├── spgxlog.h
            │   │   │   ├── stratnum.h
            │   │   │   ├── subtrans.h
            │   │   │   ├── syncscan.h
            │   │   │   ├── sysattr.h
            │   │   │   ├── tableam.h
            │   │   │   ├── table.h
            │   │   │   ├── timeline.h
            │   │   │   ├── toast_compression.h
            │   │   │   ├── toast_helper.h
            │   │   │   ├── toast_internals.h
            │   │   │   ├── transam.h
            │   │   │   ├── tsmapi.h
            │   │   │   ├── tupconvert.h
            │   │   │   ├── tupdesc_details.h
            │   │   │   ├── tupdesc.h
            │   │   │   ├── tupmacs.h
            │   │   │   ├── twophase.h
            │   │   │   ├── twophase_rmgr.h
            │   │   │   ├── valid.h
            │   │   │   ├── visibilitymapdefs.h
            │   │   │   ├── visibilitymap.h
            │   │   │   ├── xact.h
            │   │   │   ├── xlogarchive.h
            │   │   │   ├── xlogdefs.h
            │   │   │   ├── xlog.h
            │   │   │   ├── xloginsert.h
            │   │   │   ├── xlog_internal.h
            │   │   │   ├── xlogprefetcher.h
            │   │   │   ├── xlogreader.h
            │   │   │   ├── xlogrecord.h
            │   │   │   ├── xlogrecovery.h
            │   │   │   ├── xlogstats.h
            │   │   │   └── xlogutils.h
            │   │   ├── bootstrap
            │   │   │   └── bootstrap.h
            │   │   ├── catalog
            │   │   │   ├── binary_upgrade.h
            │   │   │   ├── catalog.h
            │   │   │   ├── catversion.h
            │   │   │   ├── dependency.h
            │   │   │   ├── genbki.h
            │   │   │   ├── heap.h
            │   │   │   ├── index.h
            │   │   │   ├── indexing.h
            │   │   │   ├── namespace.h
            │   │   │   ├── objectaccess.h
            │   │   │   ├── objectaddress.h
            │   │   │   ├── partition.h
            │   │   │   ├── pg_aggregate_d.h
            │   │   │   ├── pg_aggregate.h
            │   │   │   ├── pg_am_d.h
            │   │   │   ├── pg_am.h
            │   │   │   ├── pg_amop_d.h
            │   │   │   ├── pg_amop.h
            │   │   │   ├── pg_amproc_d.h
            │   │   │   ├── pg_amproc.h
            │   │   │   ├── pg_attrdef_d.h
            │   │   │   ├── pg_attrdef.h
            │   │   │   ├── pg_attribute_d.h
            │   │   │   ├── pg_attribute.h
            │   │   │   ├── pg_authid_d.h
            │   │   │   ├── pg_authid.h
            │   │   │   ├── pg_auth_members_d.h
            │   │   │   ├── pg_auth_members.h
            │   │   │   ├── pg_cast_d.h
            │   │   │   ├── pg_cast.h
            │   │   │   ├── pg_class_d.h
            │   │   │   ├── pg_class.h
            │   │   │   ├── pg_collation_d.h
            │   │   │   ├── pg_collation.h
            │   │   │   ├── pg_constraint_d.h
            │   │   │   ├── pg_constraint.h
            │   │   │   ├── pg_control.h
            │   │   │   ├── pg_conversion_d.h
            │   │   │   ├── pg_conversion.h
            │   │   │   ├── pg_database_d.h
            │   │   │   ├── pg_database.h
            │   │   │   ├── pg_db_role_setting_d.h
            │   │   │   ├── pg_db_role_setting.h
            │   │   │   ├── pg_default_acl_d.h
            │   │   │   ├── pg_default_acl.h
            │   │   │   ├── pg_depend_d.h
            │   │   │   ├── pg_depend.h
            │   │   │   ├── pg_description_d.h
            │   │   │   ├── pg_description.h
            │   │   │   ├── pg_enum_d.h
            │   │   │   ├── pg_enum.h
            │   │   │   ├── pg_event_trigger_d.h
            │   │   │   ├── pg_event_trigger.h
            │   │   │   ├── pg_extension_d.h
            │   │   │   ├── pg_extension.h
            │   │   │   ├── pg_foreign_data_wrapper_d.h
            │   │   │   ├── pg_foreign_data_wrapper.h
            │   │   │   ├── pg_foreign_server_d.h
            │   │   │   ├── pg_foreign_server.h
            │   │   │   ├── pg_foreign_table_d.h
            │   │   │   ├── pg_foreign_table.h
            │   │   │   ├── pg_index_d.h
            │   │   │   ├── pg_index.h
            │   │   │   ├── pg_inherits_d.h
            │   │   │   ├── pg_inherits.h
            │   │   │   ├── pg_init_privs_d.h
            │   │   │   ├── pg_init_privs.h
            │   │   │   ├── pg_language_d.h
            │   │   │   ├── pg_language.h
            │   │   │   ├── pg_largeobject_d.h
            │   │   │   ├── pg_largeobject.h
            │   │   │   ├── pg_largeobject_metadata_d.h
            │   │   │   ├── pg_largeobject_metadata.h
            │   │   │   ├── pg_namespace_d.h
            │   │   │   ├── pg_namespace.h
            │   │   │   ├── pg_opclass_d.h
            │   │   │   ├── pg_opclass.h
            │   │   │   ├── pg_operator_d.h
            │   │   │   ├── pg_operator.h
            │   │   │   ├── pg_opfamily_d.h
            │   │   │   ├── pg_opfamily.h
            │   │   │   ├── pg_parameter_acl_d.h
            │   │   │   ├── pg_parameter_acl.h
            │   │   │   ├── pg_partitioned_table_d.h
            │   │   │   ├── pg_partitioned_table.h
            │   │   │   ├── pg_policy_d.h
            │   │   │   ├── pg_policy.h
            │   │   │   ├── pg_proc_d.h
            │   │   │   ├── pg_proc.h
            │   │   │   ├── pg_publication_d.h
            │   │   │   ├── pg_publication.h
            │   │   │   ├── pg_publication_namespace_d.h
            │   │   │   ├── pg_publication_namespace.h
            │   │   │   ├── pg_publication_rel_d.h
            │   │   │   ├── pg_publication_rel.h
            │   │   │   ├── pg_range_d.h
            │   │   │   ├── pg_range.h
            │   │   │   ├── pg_replication_origin_d.h
            │   │   │   ├── pg_replication_origin.h
            │   │   │   ├── pg_rewrite_d.h
            │   │   │   ├── pg_rewrite.h
            │   │   │   ├── pg_seclabel_d.h
            │   │   │   ├── pg_seclabel.h
            │   │   │   ├── pg_sequence_d.h
            │   │   │   ├── pg_sequence.h
            │   │   │   ├── pg_shdepend_d.h
            │   │   │   ├── pg_shdepend.h
            │   │   │   ├── pg_shdescription_d.h
            │   │   │   ├── pg_shdescription.h
            │   │   │   ├── pg_shseclabel_d.h
            │   │   │   ├── pg_shseclabel.h
            │   │   │   ├── pg_statistic_d.h
            │   │   │   ├── pg_statistic_ext_data_d.h
            │   │   │   ├── pg_statistic_ext_data.h
            │   │   │   ├── pg_statistic_ext_d.h
            │   │   │   ├── pg_statistic_ext.h
            │   │   │   ├── pg_statistic.h
            │   │   │   ├── pg_subscription_d.h
            │   │   │   ├── pg_subscription.h
            │   │   │   ├── pg_subscription_rel_d.h
            │   │   │   ├── pg_subscription_rel.h
            │   │   │   ├── pg_tablespace_d.h
            │   │   │   ├── pg_tablespace.h
            │   │   │   ├── pg_transform_d.h
            │   │   │   ├── pg_transform.h
            │   │   │   ├── pg_trigger_d.h
            │   │   │   ├── pg_trigger.h
            │   │   │   ├── pg_ts_config_d.h
            │   │   │   ├── pg_ts_config.h
            │   │   │   ├── pg_ts_config_map_d.h
            │   │   │   ├── pg_ts_config_map.h
            │   │   │   ├── pg_ts_dict_d.h
            │   │   │   ├── pg_ts_dict.h
            │   │   │   ├── pg_ts_parser_d.h
            │   │   │   ├── pg_ts_parser.h
            │   │   │   ├── pg_ts_template_d.h
            │   │   │   ├── pg_ts_template.h
            │   │   │   ├── pg_type_d.h
            │   │   │   ├── pg_type.h
            │   │   │   ├── pg_user_mapping_d.h
            │   │   │   ├── pg_user_mapping.h
            │   │   │   ├── schemapg.h
            │   │   │   ├── storage.h
            │   │   │   ├── storage_xlog.h
            │   │   │   ├── system_fk_info.h
            │   │   │   └── toasting.h
            │   │   ├── c.h
            │   │   ├── commands
            │   │   │   ├── alter.h
            │   │   │   ├── async.h
            │   │   │   ├── cluster.h
            │   │   │   ├── collationcmds.h
            │   │   │   ├── comment.h
            │   │   │   ├── conversioncmds.h
            │   │   │   ├── copyfrom_internal.h
            │   │   │   ├── copy.h
            │   │   │   ├── createas.h
            │   │   │   ├── dbcommands.h
            │   │   │   ├── dbcommands_xlog.h
            │   │   │   ├── defrem.h
            │   │   │   ├── discard.h
            │   │   │   ├── event_trigger.h
            │   │   │   ├── explain.h
            │   │   │   ├── extension.h
            │   │   │   ├── lockcmds.h
            │   │   │   ├── matview.h
            │   │   │   ├── policy.h
            │   │   │   ├── portalcmds.h
            │   │   │   ├── prepare.h
            │   │   │   ├── proclang.h
            │   │   │   ├── progress.h
            │   │   │   ├── publicationcmds.h
            │   │   │   ├── schemacmds.h
            │   │   │   ├── seclabel.h
            │   │   │   ├── sequence.h
            │   │   │   ├── subscriptioncmds.h
            │   │   │   ├── tablecmds.h
            │   │   │   ├── tablespace.h
            │   │   │   ├── trigger.h
            │   │   │   ├── typecmds.h
            │   │   │   ├── user.h
            │   │   │   ├── vacuum.h
            │   │   │   ├── variable.h
            │   │   │   └── view.h
            │   │   ├── common
            │   │   │   ├── archive.h
            │   │   │   ├── base64.h
            │   │   │   ├── checksum_helper.h
            │   │   │   ├── compression.h
            │   │   │   ├── config_info.h
            │   │   │   ├── connect.h
            │   │   │   ├── controldata_utils.h
            │   │   │   ├── cryptohash.h
            │   │   │   ├── fe_memutils.h
            │   │   │   ├── file_perm.h
            │   │   │   ├── file_utils.h
            │   │   │   ├── hashfn.h
            │   │   │   ├── hmac.h
            │   │   │   ├── int128.h
            │   │   │   ├── int.h
            │   │   │   ├── ip.h
            │   │   │   ├── jsonapi.h
            │   │   │   ├── keywords.h
            │   │   │   ├── kwlookup.h
            │   │   │   ├── link-canary.h
            │   │   │   ├── logging.h
            │   │   │   ├── md5.h
            │   │   │   ├── openssl.h
            │   │   │   ├── pg_lzcompress.h
            │   │   │   ├── pg_prng.h
            │   │   │   ├── relpath.h
            │   │   │   ├── restricted_token.h
            │   │   │   ├── saslprep.h
            │   │   │   ├── scram-common.h
            │   │   │   ├── sha1.h
            │   │   │   ├── sha2.h
            │   │   │   ├── shortest_dec.h
            │   │   │   ├── string.h
            │   │   │   ├── unicode_combining_table.h
            │   │   │   ├── unicode_east_asian_fw_table.h
            │   │   │   ├── unicode_norm.h
            │   │   │   ├── unicode_norm_hashfunc.h
            │   │   │   ├── unicode_normprops_table.h
            │   │   │   ├── unicode_norm_table.h
            │   │   │   └── username.h
            │   │   ├── datatype
            │   │   │   └── timestamp.h
            │   │   ├── executor
            │   │   │   ├── execAsync.h
            │   │   │   ├── execdebug.h
            │   │   │   ├── execdesc.h
            │   │   │   ├── execExpr.h
            │   │   │   ├── execParallel.h
            │   │   │   ├── execPartition.h
            │   │   │   ├── executor.h
            │   │   │   ├── functions.h
            │   │   │   ├── hashjoin.h
            │   │   │   ├── instrument.h
            │   │   │   ├── nodeAgg.h
            │   │   │   ├── nodeAppend.h
            │   │   │   ├── nodeBitmapAnd.h
            │   │   │   ├── nodeBitmapHeapscan.h
            │   │   │   ├── nodeBitmapIndexscan.h
            │   │   │   ├── nodeBitmapOr.h
            │   │   │   ├── nodeCtescan.h
            │   │   │   ├── nodeCustom.h
            │   │   │   ├── nodeForeignscan.h
            │   │   │   ├── nodeFunctionscan.h
            │   │   │   ├── nodeGather.h
            │   │   │   ├── nodeGatherMerge.h
            │   │   │   ├── nodeGroup.h
            │   │   │   ├── nodeHash.h
            │   │   │   ├── nodeHashjoin.h
            │   │   │   ├── nodeIncrementalSort.h
            │   │   │   ├── nodeIndexonlyscan.h
            │   │   │   ├── nodeIndexscan.h
            │   │   │   ├── nodeLimit.h
            │   │   │   ├── nodeLockRows.h
            │   │   │   ├── nodeMaterial.h
            │   │   │   ├── nodeMemoize.h
            │   │   │   ├── nodeMergeAppend.h
            │   │   │   ├── nodeMergejoin.h
            │   │   │   ├── nodeModifyTable.h
            │   │   │   ├── nodeNamedtuplestorescan.h
            │   │   │   ├── nodeNestloop.h
            │   │   │   ├── nodeProjectSet.h
            │   │   │   ├── nodeRecursiveunion.h
            │   │   │   ├── nodeResult.h
            │   │   │   ├── nodeSamplescan.h
            │   │   │   ├── nodeSeqscan.h
            │   │   │   ├── nodeSetOp.h
            │   │   │   ├── nodeSort.h
            │   │   │   ├── nodeSubplan.h
            │   │   │   ├── nodeSubqueryscan.h
            │   │   │   ├── nodeTableFuncscan.h
            │   │   │   ├── nodeTidrangescan.h
            │   │   │   ├── nodeTidscan.h
            │   │   │   ├── nodeUnique.h
            │   │   │   ├── nodeValuesscan.h
            │   │   │   ├── nodeWindowAgg.h
            │   │   │   ├── nodeWorktablescan.h
            │   │   │   ├── spi.h
            │   │   │   ├── spi_priv.h
            │   │   │   ├── tablefunc.h
            │   │   │   ├── tqueue.h
            │   │   │   ├── tstoreReceiver.h
            │   │   │   └── tuptable.h
            │   │   ├── extension
            │   │   │   ├── cube
            │   │   │   │   └── cubedata.h
            │   │   │   ├── hstore
            │   │   │   │   └── hstore.h
            │   │   │   ├── isn
            │   │   │   │   └── isn.h
            │   │   │   ├── ltree
            │   │   │   │   └── ltree.h
            │   │   │   └── seg
            │   │   │       └── segdata.h
            │   │   ├── fe_utils
            │   │   │   ├── archive.h
            │   │   │   ├── cancel.h
            │   │   │   ├── conditional.h
            │   │   │   ├── connect_utils.h
            │   │   │   ├── mbprint.h
            │   │   │   ├── option_utils.h
            │   │   │   ├── parallel_slot.h
            │   │   │   ├── print.h
            │   │   │   ├── psqlscan.h
            │   │   │   ├── psqlscan_int.h
            │   │   │   ├── query_utils.h
            │   │   │   ├── recovery_gen.h
            │   │   │   ├── simple_list.h
            │   │   │   └── string_utils.h
            │   │   ├── fmgr.h
            │   │   ├── foreign
            │   │   │   ├── fdwapi.h
            │   │   │   └── foreign.h
            │   │   ├── funcapi.h
            │   │   ├── getaddrinfo.h
            │   │   ├── getopt_long.h
            │   │   ├── jit
            │   │   │   ├── jit.h
            │   │   │   ├── llvmjit_emit.h
            │   │   │   └── llvmjit.h
            │   │   ├── lib
            │   │   │   ├── binaryheap.h
            │   │   │   ├── bipartite_match.h
            │   │   │   ├── bloomfilter.h
            │   │   │   ├── dshash.h
            │   │   │   ├── hyperloglog.h
            │   │   │   ├── ilist.h
            │   │   │   ├── integerset.h
            │   │   │   ├── knapsack.h
            │   │   │   ├── pairingheap.h
            │   │   │   ├── qunique.h
            │   │   │   ├── rbtree.h
            │   │   │   ├── simplehash.h
            │   │   │   ├── sort_template.h
            │   │   │   └── stringinfo.h
            │   │   ├── libpq
            │   │   │   ├── auth.h
            │   │   │   ├── be-fsstubs.h
            │   │   │   ├── be-gssapi-common.h
            │   │   │   ├── crypt.h
            │   │   │   ├── hba.h
            │   │   │   ├── ifaddr.h
            │   │   │   ├── libpq-be.h
            │   │   │   ├── libpq-fs.h
            │   │   │   ├── libpq.h
            │   │   │   ├── pqcomm.h
            │   │   │   ├── pqformat.h
            │   │   │   ├── pqmq.h
            │   │   │   ├── pqsignal.h
            │   │   │   ├── sasl.h
            │   │   │   └── scram.h
            │   │   ├── mb
            │   │   │   ├── pg_wchar.h
            │   │   │   └── stringinfo_mb.h
            │   │   ├── miscadmin.h
            │   │   ├── nodes
            │   │   │   ├── bitmapset.h
            │   │   │   ├── execnodes.h
            │   │   │   ├── extensible.h
            │   │   │   ├── lockoptions.h
            │   │   │   ├── makefuncs.h
            │   │   │   ├── memnodes.h
            │   │   │   ├── nodeFuncs.h
            │   │   │   ├── nodes.h
            │   │   │   ├── params.h
            │   │   │   ├── parsenodes.h
            │   │   │   ├── pathnodes.h
            │   │   │   ├── pg_list.h
            │   │   │   ├── plannodes.h
            │   │   │   ├── primnodes.h
            │   │   │   ├── print.h
            │   │   │   ├── readfuncs.h
            │   │   │   ├── replnodes.h
            │   │   │   ├── subscripting.h
            │   │   │   ├── supportnodes.h
            │   │   │   ├── tidbitmap.h
            │   │   │   └── value.h
            │   │   ├── optimizer
            │   │   │   ├── appendinfo.h
            │   │   │   ├── clauses.h
            │   │   │   ├── cost.h
            │   │   │   ├── geqo_copy.h
            │   │   │   ├── geqo_gene.h
            │   │   │   ├── geqo.h
            │   │   │   ├── geqo_misc.h
            │   │   │   ├── geqo_mutation.h
            │   │   │   ├── geqo_pool.h
            │   │   │   ├── geqo_random.h
            │   │   │   ├── geqo_recombination.h
            │   │   │   ├── geqo_selection.h
            │   │   │   ├── inherit.h
            │   │   │   ├── joininfo.h
            │   │   │   ├── optimizer.h
            │   │   │   ├── orclauses.h
            │   │   │   ├── paramassign.h
            │   │   │   ├── pathnode.h
            │   │   │   ├── paths.h
            │   │   │   ├── placeholder.h
            │   │   │   ├── plancat.h
            │   │   │   ├── planmain.h
            │   │   │   ├── planner.h
            │   │   │   ├── prep.h
            │   │   │   ├── restrictinfo.h
            │   │   │   ├── subselect.h
            │   │   │   └── tlist.h
            │   │   ├── parser
            │   │   │   ├── analyze.h
            │   │   │   ├── gram.h
            │   │   │   ├── gramparse.h
            │   │   │   ├── kwlist.h
            │   │   │   ├── parse_agg.h
            │   │   │   ├── parse_clause.h
            │   │   │   ├── parse_coerce.h
            │   │   │   ├── parse_collate.h
            │   │   │   ├── parse_cte.h
            │   │   │   ├── parse_enr.h
            │   │   │   ├── parse_expr.h
            │   │   │   ├── parse_func.h
            │   │   │   ├── parse_merge.h
            │   │   │   ├── parse_node.h
            │   │   │   ├── parse_oper.h
            │   │   │   ├── parse_param.h
            │   │   │   ├── parse_relation.h
            │   │   │   ├── parser.h
            │   │   │   ├── parse_target.h
            │   │   │   ├── parsetree.h
            │   │   │   ├── parse_type.h
            │   │   │   ├── parse_utilcmd.h
            │   │   │   ├── scanner.h
            │   │   │   └── scansup.h
            │   │   ├── partitioning
            │   │   │   ├── partbounds.h
            │   │   │   ├── partdefs.h
            │   │   │   ├── partdesc.h
            │   │   │   └── partprune.h
            │   │   ├── pg_config_ext.h
            │   │   ├── pg_config.h
            │   │   ├── pg_config_manual.h
            │   │   ├── pg_config_os.h
            │   │   ├── pg_getopt.h
            │   │   ├── pgstat.h
            │   │   ├── pgtar.h
            │   │   ├── pgtime.h
            │   │   ├── pg_trace.h
            │   │   ├── plpgsql.h
            │   │   ├── port
            │   │   │   ├── aix.h
            │   │   │   ├── atomics
            │   │   │   │   ├── arch-arm.h
            │   │   │   │   ├── arch-hppa.h
            │   │   │   │   ├── arch-ia64.h
            │   │   │   │   ├── arch-ppc.h
            │   │   │   │   ├── arch-x86.h
            │   │   │   │   ├── fallback.h
            │   │   │   │   ├── generic-acc.h
            │   │   │   │   ├── generic-gcc.h
            │   │   │   │   ├── generic.h
            │   │   │   │   ├── generic-msvc.h
            │   │   │   │   └── generic-sunpro.h
            │   │   │   ├── atomics.h
            │   │   │   ├── cygwin.h
            │   │   │   ├── darwin.h
            │   │   │   ├── freebsd.h
            │   │   │   ├── hpux.h
            │   │   │   ├── linux.h
            │   │   │   ├── netbsd.h
            │   │   │   ├── openbsd.h
            │   │   │   ├── pg_bitutils.h
            │   │   │   ├── pg_bswap.h
            │   │   │   ├── pg_crc32c.h
            │   │   │   ├── pg_iovec.h
            │   │   │   ├── pg_pthread.h
            │   │   │   ├── solaris.h
            │   │   │   ├── win32
            │   │   │   │   ├── arpa
            │   │   │   │   │   └── inet.h
            │   │   │   │   ├── dlfcn.h
            │   │   │   │   ├── grp.h
            │   │   │   │   ├── netdb.h
            │   │   │   │   ├── netinet
            │   │   │   │   │   └── in.h
            │   │   │   │   ├── pwd.h
            │   │   │   │   └── sys
            │   │   │   │       ├── socket.h
            │   │   │   │       └── wait.h
            │   │   │   ├── win32.h
            │   │   │   ├── win32_msvc
            │   │   │   │   ├── dirent.h
            │   │   │   │   ├── sys
            │   │   │   │   │   ├── file.h
            │   │   │   │   │   ├── param.h
            │   │   │   │   │   └── time.h
            │   │   │   │   ├── unistd.h
            │   │   │   │   └── utime.h
            │   │   │   ├── win32ntdll.h
            │   │   │   └── win32_port.h
            │   │   ├── portability
            │   │   │   ├── instr_time.h
            │   │   │   └── mem.h
            │   │   ├── port.h
            │   │   ├── postgres_ext.h
            │   │   ├── postgres_fe.h
            │   │   ├── postgres.h
            │   │   ├── postmaster
            │   │   │   ├── autovacuum.h
            │   │   │   ├── auxprocess.h
            │   │   │   ├── bgworker.h
            │   │   │   ├── bgworker_internals.h
            │   │   │   ├── bgwriter.h
            │   │   │   ├── fork_process.h
            │   │   │   ├── interrupt.h
            │   │   │   ├── pgarch.h
            │   │   │   ├── postmaster.h
            │   │   │   ├── startup.h
            │   │   │   ├── syslogger.h
            │   │   │   └── walwriter.h
            │   │   ├── regex
            │   │   │   ├── regcustom.h
            │   │   │   ├── regerrs.h
            │   │   │   ├── regex.h
            │   │   │   ├── regexport.h
            │   │   │   └── regguts.h
            │   │   ├── replication
            │   │   │   ├── decode.h
            │   │   │   ├── logical.h
            │   │   │   ├── logicallauncher.h
            │   │   │   ├── logicalproto.h
            │   │   │   ├── logicalrelation.h
            │   │   │   ├── logicalworker.h
            │   │   │   ├── message.h
            │   │   │   ├── origin.h
            │   │   │   ├── output_plugin.h
            │   │   │   ├── pgoutput.h
            │   │   │   ├── reorderbuffer.h
            │   │   │   ├── slot.h
            │   │   │   ├── snapbuild.h
            │   │   │   ├── syncrep.h
            │   │   │   ├── walreceiver.h
            │   │   │   ├── walsender.h
            │   │   │   ├── walsender_private.h
            │   │   │   └── worker_internal.h
            │   │   ├── rewrite
            │   │   │   ├── prs2lock.h
            │   │   │   ├── rewriteDefine.h
            │   │   │   ├── rewriteHandler.h
            │   │   │   ├── rewriteManip.h
            │   │   │   ├── rewriteRemove.h
            │   │   │   ├── rewriteSearchCycle.h
            │   │   │   ├── rewriteSupport.h
            │   │   │   └── rowsecurity.h
            │   │   ├── rusagestub.h
            │   │   ├── snowball
            │   │   │   ├── header.h
            │   │   │   └── libstemmer
            │   │   │       ├── api.h
            │   │   │       ├── header.h
            │   │   │       ├── stem_ISO_8859_1_basque.h
            │   │   │       ├── stem_ISO_8859_1_catalan.h
            │   │   │       ├── stem_ISO_8859_1_danish.h
            │   │   │       ├── stem_ISO_8859_1_dutch.h
            │   │   │       ├── stem_ISO_8859_1_english.h
            │   │   │       ├── stem_ISO_8859_1_finnish.h
            │   │   │       ├── stem_ISO_8859_1_french.h
            │   │   │       ├── stem_ISO_8859_1_german.h
            │   │   │       ├── stem_ISO_8859_1_indonesian.h
            │   │   │       ├── stem_ISO_8859_1_irish.h
            │   │   │       ├── stem_ISO_8859_1_italian.h
            │   │   │       ├── stem_ISO_8859_1_norwegian.h
            │   │   │       ├── stem_ISO_8859_1_porter.h
            │   │   │       ├── stem_ISO_8859_1_portuguese.h
            │   │   │       ├── stem_ISO_8859_1_spanish.h
            │   │   │       ├── stem_ISO_8859_1_swedish.h
            │   │   │       ├── stem_ISO_8859_2_hungarian.h
            │   │   │       ├── stem_ISO_8859_2_romanian.h
            │   │   │       ├── stem_KOI8_R_russian.h
            │   │   │       ├── stem_UTF_8_arabic.h
            │   │   │       ├── stem_UTF_8_armenian.h
            │   │   │       ├── stem_UTF_8_basque.h
            │   │   │       ├── stem_UTF_8_catalan.h
            │   │   │       ├── stem_UTF_8_danish.h
            │   │   │       ├── stem_UTF_8_dutch.h
            │   │   │       ├── stem_UTF_8_english.h
            │   │   │       ├── stem_UTF_8_finnish.h
            │   │   │       ├── stem_UTF_8_french.h
            │   │   │       ├── stem_UTF_8_german.h
            │   │   │       ├── stem_UTF_8_greek.h
            │   │   │       ├── stem_UTF_8_hindi.h
            │   │   │       ├── stem_UTF_8_hungarian.h
            │   │   │       ├── stem_UTF_8_indonesian.h
            │   │   │       ├── stem_UTF_8_irish.h
            │   │   │       ├── stem_UTF_8_italian.h
            │   │   │       ├── stem_UTF_8_lithuanian.h
            │   │   │       ├── stem_UTF_8_nepali.h
            │   │   │       ├── stem_UTF_8_norwegian.h
            │   │   │       ├── stem_UTF_8_porter.h
            │   │   │       ├── stem_UTF_8_portuguese.h
            │   │   │       ├── stem_UTF_8_romanian.h
            │   │   │       ├── stem_UTF_8_russian.h
            │   │   │       ├── stem_UTF_8_serbian.h
            │   │   │       ├── stem_UTF_8_spanish.h
            │   │   │       ├── stem_UTF_8_swedish.h
            │   │   │       ├── stem_UTF_8_tamil.h
            │   │   │       ├── stem_UTF_8_turkish.h
            │   │   │       └── stem_UTF_8_yiddish.h
            │   │   ├── statistics
            │   │   │   ├── extended_stats_internal.h
            │   │   │   └── statistics.h
            │   │   ├── storage
            │   │   │   ├── backendid.h
            │   │   │   ├── barrier.h
            │   │   │   ├── block.h
            │   │   │   ├── buffile.h
            │   │   │   ├── buf.h
            │   │   │   ├── buf_internals.h
            │   │   │   ├── bufmgr.h
            │   │   │   ├── bufpage.h
            │   │   │   ├── checksum.h
            │   │   │   ├── checksum_impl.h
            │   │   │   ├── condition_variable.h
            │   │   │   ├── copydir.h
            │   │   │   ├── dsm.h
            │   │   │   ├── dsm_impl.h
            │   │   │   ├── fd.h
            │   │   │   ├── fileset.h
            │   │   │   ├── freespace.h
            │   │   │   ├── fsm_internals.h
            │   │   │   ├── indexfsm.h
            │   │   │   ├── ipc.h
            │   │   │   ├── item.h
            │   │   │   ├── itemid.h
            │   │   │   ├── itemptr.h
            │   │   │   ├── large_object.h
            │   │   │   ├── latch.h
            │   │   │   ├── lmgr.h
            │   │   │   ├── lockdefs.h
            │   │   │   ├── lock.h
            │   │   │   ├── lwlock.h
            │   │   │   ├── lwlocknames.h
            │   │   │   ├── md.h
            │   │   │   ├── off.h
            │   │   │   ├── pg_sema.h
            │   │   │   ├── pg_shmem.h
            │   │   │   ├── pmsignal.h
            │   │   │   ├── predicate.h
            │   │   │   ├── predicate_internals.h
            │   │   │   ├── procarray.h
            │   │   │   ├── proc.h
            │   │   │   ├── proclist.h
            │   │   │   ├── proclist_types.h
            │   │   │   ├── procsignal.h
            │   │   │   ├── reinit.h
            │   │   │   ├── relfilenode.h
            │   │   │   ├── sharedfileset.h
            │   │   │   ├── shmem.h
            │   │   │   ├── shm_mq.h
            │   │   │   ├── shm_toc.h
            │   │   │   ├── sinvaladt.h
            │   │   │   ├── sinval.h
            │   │   │   ├── s_lock.h
            │   │   │   ├── smgr.h
            │   │   │   ├── spin.h
            │   │   │   ├── standbydefs.h
            │   │   │   ├── standby.h
            │   │   │   └── sync.h
            │   │   ├── tcop
            │   │   │   ├── cmdtag.h
            │   │   │   ├── cmdtaglist.h
            │   │   │   ├── deparse_utility.h
            │   │   │   ├── dest.h
            │   │   │   ├── fastpath.h
            │   │   │   ├── pquery.h
            │   │   │   ├── tcopprot.h
            │   │   │   └── utility.h
            │   │   ├── tsearch
            │   │   │   ├── dicts
            │   │   │   │   ├── regis.h
            │   │   │   │   └── spell.h
            │   │   │   ├── ts_cache.h
            │   │   │   ├── ts_locale.h
            │   │   │   ├── ts_public.h
            │   │   │   ├── ts_type.h
            │   │   │   └── ts_utils.h
            │   │   ├── utils
            │   │   │   ├── aclchk_internal.h
            │   │   │   ├── acl.h
            │   │   │   ├── arrayaccess.h
            │   │   │   ├── array.h
            │   │   │   ├── ascii.h
            │   │   │   ├── attoptcache.h
            │   │   │   ├── backend_progress.h
            │   │   │   ├── backend_status.h
            │   │   │   ├── builtins.h
            │   │   │   ├── bytea.h
            │   │   │   ├── cash.h
            │   │   │   ├── catcache.h
            │   │   │   ├── combocid.h
            │   │   │   ├── date.h
            │   │   │   ├── datetime.h
            │   │   │   ├── datum.h
            │   │   │   ├── dsa.h
            │   │   │   ├── dynahash.h
            │   │   │   ├── elog.h
            │   │   │   ├── errcodes.h
            │   │   │   ├── evtcache.h
            │   │   │   ├── expandeddatum.h
            │   │   │   ├── expandedrecord.h
            │   │   │   ├── float.h
            │   │   │   ├── fmgroids.h
            │   │   │   ├── fmgrprotos.h
            │   │   │   ├── fmgrtab.h
            │   │   │   ├── formatting.h
            │   │   │   ├── freepage.h
            │   │   │   ├── geo_decls.h
            │   │   │   ├── guc.h
            │   │   │   ├── guc_tables.h
            │   │   │   ├── help_config.h
            │   │   │   ├── hsearch.h
            │   │   │   ├── index_selfuncs.h
            │   │   │   ├── inet.h
            │   │   │   ├── inval.h
            │   │   │   ├── jsonb.h
            │   │   │   ├── jsonfuncs.h
            │   │   │   ├── json.h
            │   │   │   ├── jsonpath.h
            │   │   │   ├── logtape.h
            │   │   │   ├── lsyscache.h
            │   │   │   ├── memdebug.h
            │   │   │   ├── memutils.h
            │   │   │   ├── multirangetypes.h
            │   │   │   ├── numeric.h
            │   │   │   ├── old_snapshot.h
            │   │   │   ├── palloc.h
            │   │   │   ├── partcache.h
            │   │   │   ├── pg_crc.h
            │   │   │   ├── pg_locale.h
            │   │   │   ├── pg_lsn.h
            │   │   │   ├── pg_rusage.h
            │   │   │   ├── pgstat_internal.h
            │   │   │   ├── pidfile.h
            │   │   │   ├── plancache.h
            │   │   │   ├── portal.h
            │   │   │   ├── probes.h
            │   │   │   ├── ps_status.h
            │   │   │   ├── queryenvironment.h
            │   │   │   ├── queryjumble.h
            │   │   │   ├── rangetypes.h
            │   │   │   ├── regproc.h
            │   │   │   ├── relcache.h
            │   │   │   ├── relfilenodemap.h
            │   │   │   ├── rel.h
            │   │   │   ├── relmapper.h
            │   │   │   ├── relptr.h
            │   │   │   ├── reltrigger.h
            │   │   │   ├── resowner.h
            │   │   │   ├── resowner_private.h
            │   │   │   ├── rls.h
            │   │   │   ├── ruleutils.h
            │   │   │   ├── sampling.h
            │   │   │   ├── selfuncs.h
            │   │   │   ├── sharedtuplestore.h
            │   │   │   ├── snapmgr.h
            │   │   │   ├── snapshot.h
            │   │   │   ├── sortsupport.h
            │   │   │   ├── spccache.h
            │   │   │   ├── syscache.h
            │   │   │   ├── timeout.h
            │   │   │   ├── timestamp.h
            │   │   │   ├── tuplesort.h
            │   │   │   ├── tuplestore.h
            │   │   │   ├── typcache.h
            │   │   │   ├── tzparser.h
            │   │   │   ├── uuid.h
            │   │   │   ├── varbit.h
            │   │   │   ├── varlena.h
            │   │   │   ├── wait_event.h
            │   │   │   ├── xid8.h
            │   │   │   └── xml.h
            │   │   └── windowapi.h
            │   ├── sql3types.h
            │   ├── sqlca.h
            │   ├── sqlda-compat.h
            │   ├── sqlda.h
            │   └── sqlda-native.h
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
