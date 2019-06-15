# FASTMiner-SG
Support x16r/x16s/xevan/x17/phi/tribus/aergo/polytimos/geek/skunk algos. It contains 1% dev fee. 

## This miner is rewriten SGMINER version with some fixes and new coins support
## Download it form releases

To get best perfomance start with -X 256, also you could add -g 2, to execute algos in 2 threads, it could give you better perfomance. Also use -w 256 for phi, polytimos, skunk, c11 algos

/* These options are available from commandline only */

--config|-c,load_config,"Load a JSON-format configuration file","See example.conf for an example configuration.

--default-config", set_default_config,"Specify the filename of the default config file, "Loaded at start and used when saving without a name.

--remote-config-retry",set_int_0_to_9999, opt_show_intval, &opt_remoteconf_retry, "Number of times to retry downloading remote config file. Default: 3

--remote-config-wait",set_int_0_to_9999, opt_show_intval, &opt_remoteconf_wait,
"Time in seconds to wait between download retries of remote config files. Default: 10secs"

--remote-config-usecache",opt_set_bool, &opt_remoteconf_usecache,"Use cached copy of the remote config file when download fails. Default: No",

--help|-h

--ndevs|-n,display_devs, &nDevs,"Display number of detected GPUs, OpenCL platform ","information, and exit")

--version|-V,opt_version_and_exit, packagename,Display version and exit.

/* These options are available from config file or commandline */

--algorithm|--kernel|-k,set_default_algorithm,"Set mining algorithm and most common defaults, default: scrypt"
--api-allow,set_api_allow,"Allow API access only to the given list of [G:]IP[/Prefix] addresses[/subnets]"
--api-description,set_api_description,"Description placed in the API status header, default: FASTMiner-SG version
--api-groups",set_api_groups,"API one letter groups G:cmd:cmd[,P:cmd:*...] defining the cmds a groups can use"
--api-listen",opt_set_bool, &opt_api_listen,"Enable API, default: disabled"
--api-mcast",opt_set_bool, &opt_api_mcast,"Enable API Multicast listener, default: disabled"
--api-mcast-addr",set_api_mcast_addr,"API Multicast listen address"
--api-mcast-code",set_api_mcast_code,"Code expected in the API Multicast message, don't use '-'"
--api-mcast-des",set_api_mcast_des,"Description appended to the API Multicast reply, default: ''")
--api-mcast-port",set_int_1_to_65535, opt_show_intval, &opt_api_mcast_port,"API Multicast listen port"
--api-network",opt_set_bool, &opt_api_network,"Allow API (if enabled) to listen on/for any address, default: only 127.0.0.1"
--api-port",set_int_1_to_65535, opt_show_intval, &opt_api_port,"Port number of miner API"),
--auto-fan",opt_set_bool, &opt_autofan,"Automatically adjust all GPU fan speeds to maintain a target temperature"
--auto-gpu",opt_set_bool, &opt_autoengine,"Automatically adjust all GPU engine clock speeds to maintain a target temperature"
--balance",set_balance, &pool_strategy,"Change multipool strategy from failover to even share balance"),
--blake-compact", opt_set_bool, &opt_blake_compact,"Set SPH_COMPACT_BLAKE64 for Xn derived algorithms (Can give better hashrate for some GPUs)")

--compact",opt_set_bool, &opt_compact,"Use compact display without per device statistics"

--debug|-D",enable_debug, &opt_debug,"Enable debug output"
--debug-log",opt_set_bool, &opt_debug,"Enable debug logging when stderr is redirected to file"
--default-profile",set_default_profile,"Set Default Profile"
--description",set_pool_description,"Pool description"
--device|-d",set_default_devices,"Select device to use, one value, range and/or comma separated (e.g. 0-2,4) default: all"),

--disable-rejecting",opt_set_bool, &opt_disable_pool,"Automatically disable pools that continually reject shares"

--expiry|-E",set_int_0_to_9999, opt_show_intval, &opt_expiry,"Upper bound on how many seconds after getting work we consider a share from it stale"

  // event options
--event-on",set_event_type,"Select event type to perform task on"
--event-runcmd",set_event_runcmd,"Command to perform on event"),
--event-reboot",set_event_reboot, "Reboot the system on event"),
--event-reboot-delay",set_event_reboot_delay,"Delay in seconds to wait before rebooting"
--event-quit",set_event_quit,"Quit FASTMiner-SG on event"
--event-quit-message",set_event_quit_message,"Quit message when quitting FASTMiner-SG on event"
--failover-only",opt_set_bool, &opt_fail_only,"Don't leak work to backup pools when primary pool is lagging"),
--failover-switch-delay",set_int_1_to_65535, opt_show_intval, &opt_fail_switch_delay,"Delay in seconds before switching back to a failed pool"),
--fix-protocol",opt_set_bool, &opt_fix_protocol,"Do not redirect to a different getwork protocol (eg. stratum)"),
--gpu-dyninterval",set_int_1_to_65535, opt_show_intval, &opt_dynamic_interval,"Set the refresh interval in ms for GPUs using dynamic intensity"),
--gpu-platform",set_int_0_to_9999, opt_show_intval, &opt_platform_id,"Select OpenCL platform ID to use for GPU mining"),
--gpu-threads|-g",set_default_gpu_threads, "Number of threads per GPU - one value or comma separated list (e.g. 1,2,1)"),
--gpu-engine",set_default_gpu_engine,"GPU engine (over)clock range in Mhz - one value, range and/or comma separated list (e.g. 850-900,900,750-850)"),
--gpu-fan",set_default_gpu_fan,"GPU fan percentage range - one value, range and/or comma separated list (e.g. 0-85,85,65)"),
--gpu-map",set_gpu_map,"Map OpenCL to ADL device order manually, paired CSV (e.g. 1:0,2:1 maps OpenCL 1 to ADL 0, 2 to 1)"),
--gpu-memclock",set_default_gpu_memclock,"Set the GPU memory (over)clock in Mhz - one value for all or separate by commas for per card"),
--gpu-memdiff",set_gpu_memdiff,"Set a fixed difference in clock speed between the GPU and memory in auto-gpu mode"),
--gpu-powertune",set_default_gpu_powertune,"Set the GPU powertune percentage - one value for all or separate by commas for per card"),
--gpu-reorder",opt_set_bool, &opt_reorder,"Attempt to reorder GPU devices according to PCI Bus ID"),
--gpu-vddc",set_default_gpu_vddc,"Set the GPU voltage in Volts - one value for all or separate by commas for per card"),
--hamsi-expand-big",set_int_1_to_10, opt_show_intval, &opt_hamsi_expand_big,"Set SPH_HAMSI_EXPAND_BIG for X13 derived algorithms (1 or 4 are common)"),
--hamsi-short",opt_set_bool, &opt_hamsi_short,"Set SPH_HAMSI_SHORT for X13 derived algorithms (Can give better hashrate for some GPUs)"),
--monero|--pool-monero",set_monero, NULL,"Use Monero Cryptonight variants as appropriate"),
--keccak-unroll",set_int_0_to_9999, opt_show_intval, &opt_keccak_unroll,"Set SPH_KECCAK_UNROLL for Xn derived algorithms (Default: 0)"),
--kernelfile",set_default_kernelfile,"Set the algorithm kernel source file (without file extension)."),
--lookup-gap",set_default_lookup_gap,"Set GPU lookup gap for scrypt mining, comma separated"),
--luffa-parallel",opt_set_bool, &opt_luffa_parallel,"Set SPH_LUFFA_PARALLEL for Xn derived algorithms (Can give better hashrate for some GPUs)"),
--benchmark",opt_set_bool, &opt_benchmark,"Enables benchmark mode for x16r/x16s. Hardcodes the hash order to run each hash function exactly once"),
 
