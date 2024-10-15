# DISA STiG enforcement for Windows


#### Table of Contents

- [DISA STiG enforcement for Windows](#disa-stig-enforcement-for-windows)
      - [Table of Contents](#table-of-contents)
  - [Description](#description)
  - [Setup](#setup)
    - [Setup Requirements](#setup-requirements)
    - [Beginning with simp\_enterprise\_windows\_disa](#beginning-with-simp_enterprise_windows_disa)
  - [Usage](#usage)
  - [Limitations](#limitations)

## Description

Provides SIMP Compliance Engine compatible data that translates to Puppet resources which will configure the target system per the Defence Information Systems Agency's Security Technical Implementation Guide.

## Setup

### Setup Requirements

This module requires the functionality provided in the simp_windows module to translate the data into puppet parameters.

### Beginning with simp_enterprise_windows_disa

Copy the module files into your Puppet modules directory.

## Usage

With the simp_windows module and its dependencies installed, specify one or more of the following profiles for enforcement by simp/compliance_markup:

* disa:mac-1:classified
* disa:mac-1:public
* disa:mac-1:sensitive
* disa:mac-2:classified
* disa:mac-2:public
* disa:mac-2:sensitive
* disa:mac-3:classified
* disa:mac-3:public
* disa:mac-3:sensitive

### Example

```puppet
include 'simp_windows'

compliance_markup::enforcement:
  - disa:mac-1:classified
```

## Limitations

This module has been tested and is supported on Domain Controllers, Domain Members, and standalone systems running the following Windows versions:

* Windows Server 2016
* Windows Server 2019
* Windows Server 2022

In addition, the following Windows workstation versions are supported:

* Windows 10
* Windows 11
