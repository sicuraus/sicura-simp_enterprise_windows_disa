# DISA STiG enforcement for Windows


#### Table of Contents

1. [Description](#description)
2. [Setup - The basics of getting started with simp_enterprise_windows_disa](#setup)
    * [Setup requirements](#setup-requirements)
    * [Beginning with simp_enterprise_windows_disa](#beginning-with-simp_enterprise_windows_disa)
3. [Usage - Configuration options and additional functionality](#usage)
4. [Limitations - OS compatibility, etc.](#limitations)
5. [Development - Guide for contributing to the module](#development)

## Description

Provides SIMP Compliance Engine compatible data that translates to Puppet resources which will configure the target system per the Defence Information Systems Agency's Security Technical Implementation Guide.

## Setup

### Setup Requirements

This module requires the functionality provided in the simp_windows module to translate the data into puppet parameters.

### Beginning with simp_enterprise_windows_disa

Copy the module files into your Puppet modules directory.
## Usage

With the simp_windows module and its dependencies installed, specify one or more of the following profiles for enforcement by simp/compliance_markup.

*   disa_stig:xccdf_mil.disa.stig_profile_mac-1_classified:
*   disa_stig:xccdf_mil.disa.stig_profile_mac-1_public:
*   disa_stig:xccdf_mil.disa.stig_profile_mac-1_sensitive:
*   disa_stig:xccdf_mil.disa.stig_profile_mac-2_classified:
*   disa_stig:xccdf_mil.disa.stig_profile_mac-2_public:
*   disa_stig:xccdf_mil.disa.stig_profile_mac-2_sensitive:
*   disa_stig:xccdf_mil.disa.stig_profile_mac-3_classified:
*   disa_stig:xccdf_mil.disa.stig_profile_mac-3_public:
*   disa_stig:xccdf_mil.disa.stig_profile_mac-3_sensitive:
*   disa_stig:xccdf_mil.disa.stig_profile_disable_slow_rules:
*   disa_stig:xccdf_mil.disa.stig_profile_cat_i_only:

```puppet
include '::simp_windows'

compliance_markup::enforcement:
  - disa_stig:xccdf_mil.disa.stig_profile_mac-1_classified
  - disa_stig:xccdf_mil.disa.stig_profile_disable_slow_rules

```

## Limitations

This module has been tested and is supported on Domain Controllers, Domain Members, and standalone systems running the following Windows versions:

* Windows 2012 R2
* Windows Server 2016 (v1607)
* Windows Server 2019 (v1809)
