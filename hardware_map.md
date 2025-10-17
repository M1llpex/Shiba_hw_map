Peripheral/Region         Physical Address Range                           Size 
------------------------ ------------------------------------------------- --------
pkvm_guest_firmware      $0x000000008b000000$..$0x000000008b0bffff$        768 KiB
gxp_mcu_fw               $0x0000000092000000$..$0x00000000923fffff$        4096 KiB
tpu_fw                   $0x0000000093000000$..$0x0000000093ffffff$        16384 KiB
aoc                      $0x0000000094000000$..$0x0000000096ffffff$        49152 KiB
sec_dram                 $0x00000000b6200000$..$0x00000000bfffffff$        161792 KiB
sec_pt                   $0x00000000e0000000$..$0x00000000e37fffff$        57344 KiB
abl                      $0x00000000f8800000$..$0x00000000f97fffff$        16384 KiB
ramoops_mem              $0x00000000fd3ff000$..$0x00000000fd7fefff$        4096 KiB
mfc_fw                   $0x00000000ffdf0000$..$0x00000000ffffffff$        2112 KiB
gcma_camera              $0x00000009c9000000$..$0x00000009cf3fffff$        102400 KiB
vframe                   $0x00000009dac00000$..$0x00000009fabfffff$        524288 KiB

A 72 MiB CMA pool was created at address $0x00000009fac00000$ for the vstream component.
A 512 MiB CMA pool was created at address $0x00000009dac00000$ for the vframe` component.
An additional 16 MiB CMA pool was reserved at address $0x00000000fc000000$

the main usable DRAM is located within a single memory node (node 0) and spans the physical address range from $0x0000000080000000$ to $0x00000009ffffffff$.


Absolute Symbols (Type A)

Address            Symbol
------------------ -------------------------
0000000000000000   _kernel_flags_le_hi32
0000000000000000   _kernel_size_le_hi32
000000000000000a   _kernel_flags_le_lo32

Debugging Symbols (Type n)

Address            Symbol
------------------ ---------------
0000000000000013   _efistub$d.10
0000000000000013   _efistub$d.11
0000000000000013   _efistub$d.4
0000000000000013   _efistub$d.5
0000000000000013   _efistub$d.6



Read-Only Data Symbols (Types r, R)
 * Type r: Local scope (visible only within its own file).
 * Type R: Global scope (visible across the entire program).

Address               Symbol                         Type
--------------------- ------------------------------ ------
ffffffffc0080000a0    .L.str                         r
ffffffffc0080000a8    .L.str.1                       r
ffffffffc0080000b0    .L.str.2                       r
ffffffffc0080000b8    .L.str.3                       r
ffffffffc0080000c0    .L.str.4                       r
ffffffffc0080000c8    .L.str.5                       r
ffffffffc0080000d0    .L.str.6                       r
ffffffffc0080000d8    .L.str.7                       r
ffffffffc0080000e0    .L.str.8                       r
ffffffffc009e20000    __end_rodata_hpage_align       R
ffffffffc009e20000    __init_end                     R
ffffffffc009e20000    __bss_start                    R
ffffffffc009e20000    __bss_begin                    R
ffffffffc009e21000    __end_of_kernel_reserve        R
ffffffffc009e21020    linux_banner                   R



Text (Code) Symbols (Types t, T)
 * Type t: Local scope (e.g., static functions).
 * Type T: Global scope (e.g., functions callable from anywhere).

Address               Symbol                     Type
--------------------- -------------------------- ------
ffffffffc008080000    startup_64                 t
ffffffffc008080084    secondary_startup_64       t
ffffffffc008080120    .L0                        t
ffffffffc008080120    .L2                        t
ffffffffc0080801a0    .L10                       t
ffffffffc0080801b0    .L11                       t
ffffffffc0080801c0    cr4_read_shadow            t
ffffffffc0080801d0    load_ucode_bsp             t
ffffffffc008080200    _start                     T
ffffffffc008080200    phys_startup_64            T
ffffffffc008080320    verify_cpu                 T
ffffffffc008080350    start_kernel               T
ffffffffc0080803b0    secondary_start_kernel     T
ffffffffc008080410    crush_nmi_handler          T
ffffffffc008080440    startup_32_smp             T



Initialized Data Symbols (Types d, D)
 * Type d: Local scope.
 * Type D: Global scope.

Address               Symbol                                Type
--------------------- ------------------------------------- ------
ffffffffc00a220ea0    saved_command_line.early_cmdline      d
ffffffffc00a220fa0    boot_params.c.0                       d
ffffffffc00a222000    trampoline_pgd                        d
ffffffffc00a223000    trampoline_pmd                        d
ffffffffc00a224000    trampoline_pte                        d
ffffffffc00a225000    idt_table                             d
ffffffffc00a226000    early_gdt_descr                       d
ffffffffc00a220000    __init_begin                          D
ffffffffc00a220000    __setup_start                         D
ffffffffc00a220000    __nosave_begin                        D
ffffffffc00a220000    __vvar_begin                          D
ffffffffc00a220e80    boot_command_line                     D
ffffffffc00a220f80    saved_command_line                    D



BSS (Uninitialized Data) Symbols (Types b, B)
 * Type b: Local scope.
 * Type B: Global scope.

Address               Symbol                                      Type
--------------------- ------------------------------------------- ------
ffffffffc00a303d28    devlink_resource_size_get.__key             b
ffffffffc00a303d29    devlink_resource_occ_get.__key              b
ffffffffc00a303d30    __devlink_trap_group_register.__key         b
ffffffffc00a303d40    devl_rate_nodes_destroy.devlink_rate        b
ffffffffc00a303d48    devl_rate_nodes_destroy.tmp                 b
ffffffffc00a303d50    devlink_linecard_create.__key               b
ffffffffc00a303d51    devl_region_create.__key                    b
ffffffffc00a303d52    devlink_port_region_create.__key            b
ffffffffc00a303d53    __devlink_health_reporter_create.__key      b
ffffffffc00a303d58    devlink_rate_node_get_by_name.devlink_rate  b
ffffffffc00a303d60    init_completion.__key                       b
ffffffffc00a303d64    wireless_seq_printf_stats.nullstats         b
ffffffffc00a303d88    net_sysctl_init.empty                       b
ffffffffc00a303dc8    net_header                                  b
ffffffffc00a305d48    transport_dgram                             b
ffffffffc00a305d50    transport_local                             b
ffffffffc00a305d58    transport_h2g                               b
ffffffffc00a305d60    transport_g2h                               b
ffffffffc00a303dd0    vsock_bind_table                            B
ffffffffc00a304d90    vsock_connected_table                       B
ffffffffc00a305d40    vsock_table_lock                            B
ffffffffc00a306000    x86_level4_pgt                              B
ffffffffc00a307000    empty_zero_page                             B
