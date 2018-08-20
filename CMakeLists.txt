cmake_minimum_required(VERSION 3.9)
project(lsm_trie)

find_package (Threads)
find_library(SSL_LIB libssl.a REQUIRED)
find_library(CRYPTO_LIB libcrypto.a REQUIRED)
find_library(MATH_LIB libmath.a REQUIRED)


set(CMAKE_CXX_STANDARD 11)


add_executable(cmap_test
        src/cmap.c
        src/cmap.h
        src/generator.h
        src/generator.c
        src/cmap_test.c
        )

target_link_libraries (cmap_test
        m
        ${CMAKE_THREAD_LIBS_INIT}
        ${SSL_LIB}
        ${CRYPTO_LIB}
        )





add_executable(generator_test
        src/generator.c
        src/generator.h
        src/generator_test.c
        src/debug.c
        src/debug.h
        )

target_link_libraries (generator_test
        m
        ${CMAKE_THREAD_LIBS_INIT}
        ${SSL_LIB}
        ${CRYPTO_LIB}
        )




add_executable(rwlock_test
        src/rwlock.c
        src/rwlock.h
        src/rwlock_test.c
        )

target_link_libraries (rwlock_test
        m
        ${CMAKE_THREAD_LIBS_INIT}
        ${SSL_LIB}
        ${CRYPTO_LIB}
        )




add_executable(mixed_test
        src/mixed_test.c
        src/debug.h
        src/debug.c
        src/stat.h
        src/stat.c
        src/generator.c
        src/generator.h
        src/db.c
        src/db.h
        src/table.c
        src/table.h
        src/rwlock.c
        src/rwlock.h
        src/bloom.c
        src/bloom.h
        src/mempool.h
        src/mempool.c
        src/coding.h
        src/coding.c
        src/cmap.c
        src/cmap.h
        src/conc.c
        src/conc.h
        )

target_link_libraries (mixed_test
        m
        ${CMAKE_THREAD_LIBS_INIT}
        ${SSL_LIB}
        ${CRYPTO_LIB}
        )




add_executable(io_util
        src/io_util.c
        src/debug.h
        src/debug.c
        src/stat.h
        src/stat.c
        src/generator.c
        src/generator.h
        )

target_link_libraries (io_util
        m
        ${CMAKE_THREAD_LIBS_INIT}
        ${SSL_LIB}
        ${CRYPTO_LIB}
        )



add_executable(cm_util
        src/cm_util.c
        src/cmap.h
        src/cmap.c
        src/generator.c
        src/generator.h
        )

target_link_libraries (cm_util
        m
        ${CMAKE_THREAD_LIBS_INIT}
        ${SSL_LIB}
        ${CRYPTO_LIB}
        )




add_executable(seqio_util
        src/seqio_util.c
        src/debug.h
        src/debug.c
        src/stat.h
        src/stat.c
        )

target_link_libraries (seqio_util
        m
        ${CMAKE_THREAD_LIBS_INIT}
        ${SSL_LIB}
        ${CRYPTO_LIB}
        )





add_executable(staged_read
        src/staged_read.c
        src/debug.c
        src/debug.h
        src/db.h
        src/db.c
        src/generator.h
        src/generator.c
        src/stat.c
        src/stat.h
        src/cmap.h
        src/cmap.c
        src/rwlock.h
        src/rwlock.c
        src/table.h
        src/table.c
        src/bloom.h
        src/bloom.c
        src/coding.c
        src/coding.h
        src/mempool.c
        src/mempool.h
        src/conc.h
        src/conc.c
        )

target_link_libraries (staged_read
        m
        ${CMAKE_THREAD_LIBS_INIT}
        ${SSL_LIB}
        ${CRYPTO_LIB}
        )









add_executable(table_test
        src/table_test.c
        src/debug.h
        src/debug.c
        src/generator.c
        src/generator.h
        src/mempool.h
        src/mempool.c
        src/table.c
        src/table.h
        src/bloom.c
        src/bloom.h
        src/coding.h
        src/coding.c
        src/stat.h
        src/stat.c
        )

target_link_libraries (table_test
        m
        ${CMAKE_THREAD_LIBS_INIT}
        ${SSL_LIB}
        ${CRYPTO_LIB}
        )




add_executable(bloom_test
        src/bloom.c
        src/bloom.h
        src/bloom_test.c
        src/mempool.c
        src/mempool.h
        src/coding.c
        src/coding.h
        src/stat.c
        src/stat.h
        src/generator.h
        src/generator.c
        src/debug.c
        src/debug.h
        )

target_link_libraries (bloom_test
        m
        ${CMAKE_THREAD_LIBS_INIT}
        ${SSL_LIB}
        ${CRYPTO_LIB}
        )
