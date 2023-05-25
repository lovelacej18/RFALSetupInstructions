```
rfal@rfal-Precision-3541:/usr/local/zed/tools$ ./ZED_Depth_Viewer 
in bool ImageHandler::initialize(sl::Mat&) : Err [999]: unknown error.
Stack trace (most recent call last):
#26   Object "[0xffffffffffffffff]", at 0xffffffffffffffff, in 
#25   Object "./ZED_Depth_Viewer", at 0x55bb83679b0d, in 
#24   Object "/lib/x86_64-linux-gnu/libc.so.6", at 0x7f7db3c8d082, in __libc_start_main
#23   Object "./ZED_Depth_Viewer", at 0x55bb83678f84, in 
#22   Object "/lib/x86_64-linux-gnu/libQt5Core.so.5", at 0x7f7db4434115, in QCoreApplication::exec()
#21   Object "/lib/x86_64-linux-gnu/libQt5Core.so.5", at 0x7f7db442c3aa, in QEventLoop::exec(QFlags<QEventLoop::ProcessEventsFlag>)
#20   Object "/lib/x86_64-linux-gnu/libQt5Core.so.5", at 0x7f7db4485434, in QEventDispatcherGlib::processEvents(QFlags<QEventLoop::ProcessEventsFlag>)
#19   Object "/lib/x86_64-linux-gnu/libglib-2.0.so.0", at 0x7f7db26a94a2, in g_main_context_iteration
#18   Object "/lib/x86_64-linux-gnu/libglib-2.0.so.0", at 0x7f7db26a93ff, in 
#17   Object "/lib/x86_64-linux-gnu/libglib-2.0.so.0", at 0x7f7db26a917c, in g_main_context_dispatch
#16   Object "/lib/x86_64-linux-gnu/libQt5Core.so.5", at 0x7f7db448506b, in 
#15   Object "/lib/x86_64-linux-gnu/libQt5Core.so.5", at 0x7f7db448477f, in QTimerInfoList::activateTimers()
#14   Object "/lib/x86_64-linux-gnu/libQt5Core.so.5", at 0x7f7db442d809, in QCoreApplication::notifyInternal2(QObject*, QEvent*)
#13   Object "/lib/x86_64-linux-gnu/libQt5Widgets.so.5", at 0x7f7db4e510ef, in QApplication::notify(QObject*, QEvent*)
#12   Object "/lib/x86_64-linux-gnu/libQt5Widgets.so.5", at 0x7f7db4e47a65, in QApplicationPrivate::notify_helper(QObject*, QEvent*)
#11   Object "/lib/x86_64-linux-gnu/libQt5Core.so.5", at 0x7f7db4459bc4, in QObject::event(QEvent*)
#10   Object "/lib/x86_64-linux-gnu/libQt5Core.so.5", at 0x7f7db44663ed, in QTimer::timeout(QTimer::QPrivateSignal)
#9    Object "/lib/x86_64-linux-gnu/libQt5Core.so.5", at 0x7f7db44591cf, in QMetaObject::activate(QObject*, int, int, void**)
#8    Object "./ZED_Depth_Viewer", at 0x55bb8367a027, in 
#7    Object "./ZED_Depth_Viewer", at 0x55bb8369ef7d, in 
#6    Object "./ZED_Depth_Viewer", at 0x55bb8369eb43, in 
#5    Object "./ZED_Depth_Viewer", at 0x55bb8369a625, in 
#4    Object "./ZED_Depth_Viewer", at 0x55bb836a8d95, in 
#3    Object "./ZED_Depth_Viewer", at 0x55bb836a7412, in 
#2    Object "./ZED_Depth_Viewer", at 0x55bb83707495, in 
#1    Object "./ZED_Depth_Viewer", at 0x55bb836c449d, in 
#0    Object "/lib/x86_64-linux-gnu/libcuda.so.1", at 0x7f7dbdaf876f, in 
Segmentation fault (Signal sent by the kernel [(nil)])
Segmentation fault (core dumped)
rfal@rfal-Precision-3541:/usr/local/zed/tools$ ./ZED_Sensor_Viewer 
QOpenGLVertexArrayObject::destroy() failed to restore current context
rfal@rfal-Precision-3541:/usr/local/zed/tools$ ./ZEDfu
 CUDA Initialisation failed :  cudaErrorUnknown
Stack trace (most recent call last) in thread 4822:
#10   Object "[0xffffffffffffffff]", at 0xffffffffffffffff, in 
#9    Object "/lib/x86_64-linux-gnu/libc.so.6", at 0x7f72d79e1132, in clone
#8    Object "/lib/x86_64-linux-gnu/libpthread.so.0", at 0x7f72d78a7608, in 
#7    Object "/lib/x86_64-linux-gnu/libQt5Core.so.5", at 0x7f72d7ec09b9, in 
#6    Object "/lib/x86_64-linux-gnu/libQt5Core.so.5", at 0x7f72d7ebe5ad, in QThread::started(QThread::QPrivateSignal)
#5    Object "/lib/x86_64-linux-gnu/libQt5Core.so.5", at 0x7f72d80b41cf, in QMetaObject::activate(QObject*, int, int, void**)
#4    Object "./ZEDfu", at 0x55d9b5a67cbf, in 
#3    Object "./ZEDfu", at 0x55d9b5a66d7f, in 
#2    Object "/usr/local/zed/lib/libsl_zed.so", at 0x7f72dbcd2f7a, in sl::Mesh::filter(sl::MeshFilterParameters, bool)
#1    Object "/usr/local/zed/lib/libsl_zed.so", at 0x7f72dbbd8d38, in 
#0    Object "/usr/local/zed/lib/libsl_zed.so", at 0x7f72dbb91dd7, in 
Segmentation fault (Address not mapped to object [(nil)])
Segmentation fault (core dumped)
```
