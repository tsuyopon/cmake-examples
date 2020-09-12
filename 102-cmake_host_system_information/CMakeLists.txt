cmake_minimum_required(VERSION 3.5)

# Set the project name
project (hello_cmake)

# cmake_host_system_information()とは、メモリ量やCPUのコア数、ホスト名などシステム情報を取得するコマンドです
# see: https://qiita.com/mrk_21/items/5e7ca775b463a4141a58
cmake_host_system_information(RESULT logical_cores QUERY NUMBER_OF_LOGICAL_CORES)
cmake_host_system_information(RESULT physical_cores QUERY NUMBER_OF_PHYSICAL_CORES)
cmake_host_system_information(RESULT hostname QUERY HOSTNAME)
cmake_host_system_information(RESULT total_vir_mem QUERY TOTAL_VIRTUAL_MEMORY)
cmake_host_system_information(RESULT avail_vir_mem QUERY AVAILABLE_VIRTUAL_MEMORY)
cmake_host_system_information(RESULT total_phys_mem QUERY TOTAL_PHYSICAL_MEMORY)
cmake_host_system_information(RESULT avail_phys_mem QUERY AVAILABLE_PHYSICAL_MEMORY)
message("NUMBER_OF_LOGICAL_CORES: ${logical_cores}") 
message("NUMBER_OF_PHYSICAL_CORES: ${physical_cores}") 
message("HOSTNAME: ${hostname}") 
message("TOTAL_VIRTUAL_MEMORY: ${total_vir_mem}") 
message("AVAILABLE_VIRTUAL_MEMORY: ${avail_vir_mem}") 
message("TOTAL_PHYSICAL_MEMORY: ${total_phys_mem}") 
message("AVAILABLE_PHYSICAL_MEMORY: ${avail_phys_mem}") 
