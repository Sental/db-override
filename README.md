## ReesSolutions DBOverride

Override Module to allow MariaDB 10.5 to 11.x support for development.
Now available via https://packagist.org/

### Use this module at your own risk in production. Versions higher than MariaDB 10.4 have no official support.

#### Version Compatibility Matrix

| MariaDB Version | Support Status              |
| --------------- | --------------------------- |
| 10.2 - 10.11    | ✅ Supported                |
| 11.x            | ✅ Supported (Experimental) |
| 11.4.8          | ✅ Tested                   |

#### Installation

- Require the Module
  `composer require reessolutions/db-override:*`

#### Configuration

The module automatically supports the following database versions:

- MySQL 5.7.x
- MySQL 8.0.x
- MariaDB 10.2-10.11
- MariaDB 11.x (including 11.4.8)

#### Usage

After installation, the module will automatically allow Magento to connect to unsupported MariaDB versions.
No additional configuration is required.

#### Troubleshooting

If you encounter issues with MariaDB 11.4.8:

1. Ensure you're using the latest version of this module
2. Clear Magento cache: `bin/magento cache:flush`
3. Check Magento logs for specific error messages
4. Verify your MariaDB installation is functioning correctly

#### Migration Notes

When upgrading from MariaDB 10.x to 11.x:

- Backup your database before upgrading
- Test in a development environment first
- Review MariaDB 11.x release notes for breaking changes
- Update your database configuration if needed

#### Support

This module is provided as-is for development purposes. For production environments,
it's recommended to use officially supported database versions.
