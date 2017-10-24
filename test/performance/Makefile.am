include $(top_srcdir)/test/Makefile.inc

TESTS_ENVIRONMENT += TEST_DIR=${builddir}

EXECUTABLES = odp_bench_packet \
	      odp_crypto \
	      odp_pktio_perf

COMPILE_ONLY = odp_l2fwd \
	       odp_pktio_ordered \
	       odp_sched_latency \
	       odp_scheduling

TESTSCRIPTS = odp_l2fwd_run.sh \
	      odp_pktio_ordered_run.sh \
	      odp_sched_latency_run.sh \
	      odp_scheduling_run.sh

TEST_EXTENSIONS = .sh

if test_perf
TESTS = $(EXECUTABLES) $(TESTSCRIPTS)
endif

bin_PROGRAMS = $(EXECUTABLES) $(COMPILE_ONLY)

odp_bench_packet_SOURCES = odp_bench_packet.c
odp_crypto_SOURCES = odp_crypto.c
odp_pktio_ordered_SOURCES = odp_pktio_ordered.c dummy_crc.h
odp_sched_latency_SOURCES = odp_sched_latency.c
odp_scheduling_SOURCES = odp_scheduling.c
odp_pktio_perf_SOURCES = odp_pktio_perf.c

dist_check_SCRIPTS = $(TESTSCRIPTS)

dist_check_DATA = udp64.pcap