---
title: caffe example
tags:
  - CNN
  - caffe
categories: CNN
date: 2016-12-24 16:14:30
---
### Rule 

all the command are excute in the cafferoot

for example `$HOME/caffe/`


<!-- more -->

### convert binaryproto to npy

```python
# convert between .binaryproto to .npy
import os
import caffe
import numpy as np
print "Usage: python convert_protomean.py proto.mean out.npy"
blob = caffe.proto.caffe_pb2.BlobProto()
BINARY_PROTO_FILE_NAME  ='imagenet_mean.binaryproto'
BINARY_PROTO_FILE_PATH  = os.path.join(os.getcwd(),BINARY_PROTO_FILE_NAME)
NPY_FILE_NAME  ='imagenet_mean.npy'
NPY_FILE_PATH  = os.path.join(os.getcwd(),NPY_FILE_NAME)

data = open( BINARY_PROTO_FILE_PATH, 'rb' ).read()
blob.ParseFromString(data)
arr = np.array( caffe.io.blobproto_to_array(blob) )
out = arr[0]
np.save( NPY_FILE_PATH , out )
```

### todo

other code like

- **lmdb**
- **create db**
- **analysis**
- **classify**
- **prototxt**
	* BN
	* NIN