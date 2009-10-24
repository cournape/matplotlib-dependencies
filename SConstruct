from os.path import \
	join as pjoin

env = DefaultEnvironment(TARGET_ARCH="x86_64")
config = env.Configure()
res = config.CheckTypeSize("int*")
if res == 4:
    print "++++++++++++++++++++++++++"
    print " 32 bits target "
    print "++++++++++++++++++++++++++"
elif res == 8:
    print "++++++++++++++++++++++++++"
    print " 64 bits target "
    print "++++++++++++++++++++++++++"
else:
    raise ValueError("Size of pointer is %d ?????" % res)
config.Finish()

env.Append(CFLAGS=["/MD", "/O1"])

env["prefix"] = "#install"
env["includedir"] = pjoin(env["prefix"], "include")
env["libdir"] = pjoin(env["prefix"], "lib")
env["bindir"] = pjoin(env["prefix"], "bin")

SConscript("zlib123/SConscript", exports="env")
SConscript("lpng1240/SConscript", exports="env")
SConscript("freetype-2.3.9/SConscript", exports="env")
