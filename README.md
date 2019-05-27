# DBR Python Extension
Version 6.5.1

This repository aims to help developers build **Python barcode** apps with [Dynamsoft Barcode Reader](https://www.dynamsoft.com/Products/Dynamic-Barcode-Reader.aspx) in Windows, Linux, macOS, and Raspberry Pi.

## License
Get the [trial license](https://www.dynamsoft.com/CustomerPortal/Portal/Triallicense.aspx).

## Contact Us
<support@dynamsoft.com>

## Environment
**Python 2/3**

## Installation
* [Dynamsoft Barcode Reader SDK](https://www.dynamsoft.com/Downloads/Dynamic-Barcode-Reader-Download.aspx).
* Download a zip of the Dynamsoft Barcode Reader Python extension
 
### Install dependencies
* OpenCV

    ```
    pip install opencv-python
    python3 -m pip install opencv-python
    ```
    
    For **Raspberry Pi**
    
    ```
    sudo apt-get install libopencv-dev python-opencv
    ```
    
* NumPy
	
    ```
    pip install numpy
    python3 -m pip install numpy
    ```
* Automatically Tuned Linear Algebra Software
    ```
    sudo apt-get install libcblas-dev
    sudo apt-get install libatlas-base-dev
    ```
* JasPer
    ```
    sudo apt-get install libjasper-dev
    ```
* Qt
    ```
    sudo apt-get install libqt4-test
    ``` 
## HowTo
### Windows
Set **Visual Studio** in **cmd.exe**. For example, **Visual Studio 2015**:

```
SET VS90COMNTOOLS=%VS140COMNTOOLS%
```

Edit `setup.py`. Replace the **dbr_lib_dir** and **dbr_dll** with yours:

```
dbr_lib_dir = r'e:\Program Files (x86)\Dynamsoft\Barcode Reader 6.5.1\Components\C_C++\Lib'
dbr_dll = r'e:\Program Files (x86)\Dynamsoft\Barcode Reader 6.5.1\Components\C_C++\Redist\x64\DynamsoftBarcodeReaderx64.dll'
```

Build and install the Python extension:

```
cd src
python setup.py build install
python3 setup.py build install
```

### Linux, macOS and Raspberry Pi
Unzip the SDK.
Copy ``libDynamsoftBarcodeReader.so`` from `{SDK}/Dynamsoft/BarcodeReader/lib` to `/usr/lib`. 
If you don't have access to `/usr/lib`, try to copy the library to `/usr/local/lib` and set the **LD_LIBRARY_PATH** as follows:

```bash
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib
```
### Build and install the Python extension:
Unzip the python project
```
cd {project}/src
sudo python setup.py build install
sudo python3 setup.py build install
```

## Examples
- examples/video
    ```
    python rtsp.py
    ```
- examples/camera
    ```
    python camera.py
    ```
- examples/command-line
    ```
    python test.py
    ```

## Related Articles
* [Things to Do with DBR 6.0 and Python Barcode Extension](http://www.codepool.biz/dynamsoft-barcode-python-extension-6-0.html)
* [How to Port C/C++ Barcode Extension to Python 3](http://www.codepool.biz/cc-barcode-extension-python-3.html)
* [Building Python Barcode Extension with DBR 5.0 on Windows](http://www.codepool.biz/python-barcode-extension-dbr-windows.html)
* [Building Python Barcode Extension with DBR 5.2 for Linux](http://www.codepool.biz/build-linux-python-barcode-extension.html)
