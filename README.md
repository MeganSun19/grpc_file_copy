# gRPC File Copy

## Overview

This script copies a file on a Cisco IOS-XR device using gRPC with yang model:Cisco-IOS-XR-shellutil-copy-act.yang.

---


## Prerequisites:
	- Install Python and Required Libraries:
      Ensure Python 3.6 or later is installed.
	- Install gRPC ibraries:
     pip install grpcio grpcio-tools protobuf

## Steps

1. **Download the Required `.proto` Files**
   - https://github.com/nleiva/xrgrpc/blob/v0.6.0/proto/ems/ems_grpc.proto
2. **Complile the '.proto' files**
   - Use `grpcio-tools` to generate Python gRPC and message classes:
     ```bash
     python3 -m grpc_tools.protoc -I. --python_out=. --grpc_python_out=. os.proto
     ```
   - Repeat this step for all required `.proto` files.
3. **Prepare JSON payload based on:**
  https://github.com/YangModels/yang/blob/main/vendor/cisco/xr/7102/Cisco-IOS-XR-shellutil-copy-act.yang

3. **Configure your environment**
	- Set Up Credentials (Optional, if using secure gRPC)
    	- Obtain the root CA certificate for the device and save it (e.g., 'CA.cer').
    	- Update the 'cert_cn' and the and certificate paths in the script as needed.
    - Set the device IP/username/password Https server IP/username/password etc.





