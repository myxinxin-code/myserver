
cc_library(
   name = "hello-server",
   srcs = glob(["timer/lst_timer.cpp", "http/http_conn.cpp", "log/log.cpp", "CGImysql/sql_connection_pool.cpp", "webserver.cpp", "config.cpp"]),
     hdrs = glob(["timer/*.h", "log/*.h", "threadpool/threadpool.h", "http/*.h", "lock/*.h", "CGImysql/*.h","config.h", "webserver.h"]),

)

cc_binary(
     name = "server",
     srcs = glob(["main.cpp"]),
     deps = [
	":hello-server",
	],
     linkopts = ["-g","-lpthread","-lmysqlclient","-std=c++11"],
)
