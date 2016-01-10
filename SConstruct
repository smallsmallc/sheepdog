import os
import sys

#Redirect build output
buildLogStdout = os.popen('tee build.log', 'w')
buildLogStderr = os.popen('tee build.err', 'w')
sys.stdout = buildLogStdout
sys.stderr = buildLogStderr

env = Environment()

Export('env')
env.SConscript('rpc/SConscript',
               variant_dir='build/bin',
              )
