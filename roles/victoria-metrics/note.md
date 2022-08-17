Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: 2022-08-12T16:20:29.013Z        info        VictoriaMetrics/lib/logger/flag.go:12        build version: vmagent-20220808-173305-tags-v1.80.0-0-gad00f4aaa
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: 2022-08-12T16:20:29.014Z        info        VictoriaMetrics/lib/logger/flag.go:13        command-line flags
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: 2022-08-12T16:20:29.014Z        info        VictoriaMetrics/lib/logger/flag.go:20          -httpListenAddr="0.0.0.0:8429"
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: 2022-08-12T16:20:29.014Z        info        VictoriaMetrics/lib/logger/flag.go:20          -promscrape.config="/etc/vmagent/vmagent.yml"
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: 2022-08-12T16:20:29.014Z        info        VictoriaMetrics/lib/logger/flag.go:20          -remoteWrite.url="secret"
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: 2022-08-12T16:20:29.014Z        info        VictoriaMetrics/app/vmagent/main.go:103        starting vmagent at "0.0.0.0:8429"...
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: 2022-08-12T16:20:29.014Z        info        VictoriaMetrics/lib/memory/memory.go:42        limiting caches to 2406130483 bytes, leaving 1604086989 bytes to the OS according to -memory.allowedPer>
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: 2022-08-12T16:20:29.014Z        error        VictoriaMetrics/lib/persistentqueue/persistentqueue.go:143        cannot open persistent queue at "vmagent-remotewrite-data/persistent-queue/1_A1034C>
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: 2022-08-12T16:20:29.014Z        panic        VictoriaMetrics/lib/persistentqueue/persistentqueue.go:147        FATAL: cannot create directory "vmagent-remotewrite-data/persistent-queue/1_A1034CE>
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: panic: FATAL: cannot create directory "vmagent-remotewrite-data/persistent-queue/1_A1034CECB2A6FE4E": mkdir vmagent-remotewrite-data: permission denied
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: goroutine 1 [running]:
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: github.com/VictoriaMetrics/VictoriaMetrics/lib/logger.logMessage({0x9fc534, 0x5}, {0xc0002deb40, 0x90}, 0x1?)
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]:         github.com/VictoriaMetrics/VictoriaMetrics/lib/logger/logger.go:269 +0x975
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: github.com/VictoriaMetrics/VictoriaMetrics/lib/logger.logLevelSkipframes(0x1, {0x9fc534, 0x5}, {0x9fdc60?, 0x20000080?}, {0xc00029f998?, 0x0?, 0xe6a160?})
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]:         github.com/VictoriaMetrics/VictoriaMetrics/lib/logger/logger.go:137 +0x1d6
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: github.com/VictoriaMetrics/VictoriaMetrics/lib/logger.logLevel(...)
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]:         github.com/VictoriaMetrics/VictoriaMetrics/lib/logger/logger.go:129
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: github.com/VictoriaMetrics/VictoriaMetrics/lib/logger.Panicf(...)
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]:         github.com/VictoriaMetrics/VictoriaMetrics/lib/logger/logger.go:125
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: github.com/VictoriaMetrics/VictoriaMetrics/lib/persistentqueue.mustOpenInternal({0xc00002a1c0, 0x3c}, {0xc0000282e0, 0xc}, 0x20000080, 0x2000000, 0x453e29?)
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]:         github.com/VictoriaMetrics/VictoriaMetrics/lib/persistentqueue/persistentqueue.go:147 +0x314
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: github.com/VictoriaMetrics/VictoriaMetrics/lib/persistentqueue.mustOpen(...)
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]:         github.com/VictoriaMetrics/VictoriaMetrics/lib/persistentqueue/persistentqueue.go:131
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: github.com/VictoriaMetrics/VictoriaMetrics/lib/persistentqueue.MustOpenFastQueue({0xc00002a1c0, 0x3c}, {0xc0000282e0?, 0x3?}, 0x3?, 0x968ac0?)
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]:         github.com/VictoriaMetrics/VictoriaMetrics/lib/persistentqueue/fastqueue.go:45 +0x65
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]: github.com/VictoriaMetrics/VictoriaMetrics/app/vmagent/remotewrite.newRemoteWriteCtx(0x0, 0xd?, 0xc0002a8120, 0x1?, {0xc0000282e0, 0xc})
Aug 12 11:20:29 vicmets.whemhome vmagent-prod[3863]:         github.com/VictoriaMetrics/VictoriaMetrics/app/vmagent/remotewrite/remotewrite.go:439 +0x1b9
