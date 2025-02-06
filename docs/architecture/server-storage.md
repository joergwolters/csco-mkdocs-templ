# Server and Storage

With documented servers, you have the option of going ‘deep’ into the details as
well as ‘up’ into the world of services and applications.
In terms of the order, the recommendation is first documenting the objects
that might end up being reused:

1. Physical servers
2. Virtual servers
3. Clusters (consisting of multiple servers)
  
## Physical servers

Document the hardware configuration, physical or virtual, and the base version from
which all configuration changes were made. Following this, the individual features
of the device must be specified. Anything that is designed to provide a specific
function but is not part of the standard is worth documenting.

- Hardware details
- Location - see preparatory work above
- Network connection - see preparatory work above
- Contact person

## Storage

Document the storage hardware configuration, physical or virtual, including the storage
design (FC, iSCSI, NFS, NVMeoF, ...). Provide management configuration, the base
firmware version from which all configuration changes were made.

- Storage configuration
- Management access
- Admin accounts
- API documentation

## Detailed server documentation

The depth of detail can be very deep: here are a few ideas about what is still
left to document:

- Operating System, software, versions
- admin accounts
- passwords used
- modification to files
- modification to configuration
- installed software (ideally incl. installation screenshots for all individual steps)
- installed licenses
- configuration changes of the installed software
