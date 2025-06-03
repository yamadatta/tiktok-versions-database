# TikTok Version Database

> **The ultimate archive of TikTok Android releases from 32.0.3 to latest**

A comprehensive, machine-readable database containing complete version history of TikTok Android app releases. Perfect for developers, security researchers, and anyone who needs accurate TikTok version data.

## What's Inside

- **90 stable releases** spanning 18+ months
- **Complete version codes** including manifest and update codes
- **Accurate release dates** sourced from APK Mirror
- **Clean JSON format** ready for integration
- **No beta builds** or lite variants cluttering the data

## Quick Stats

| Series | Versions | Time Period |
|--------|----------|-------------|
| 32.x   | 7        | Nov 2023    |
| 33.x   | 4        | Jan-Mar 2024|
| 34.x   | 3        | Mar-May 2024|
| 35.x   | 15       | May-Aug 2024|
| 36.x   | 14       | Aug-Oct 2024|
| 37.x   | 8        | Oct-Dec 2024|
| 38.x   | 1        | Jan 2025    |
| 39.x   | 18       | Apr-May 2025|
| 40.x   | 10       | May-Jun 2025|

## Data Structure

Each version entry contains:

```json
{
  "version_code": "402020",
  "version_name": "40.2.2",
  "manifest_version_code": "2025402020",
  "update_version_code": "2025402020",
  "release_date": "2025-06-01",
  "series": "40.x",
  "latest": true
}
```

## Usage Examples

### Find Latest Version
```javascript
const latest = data.tiktok_version_database.versions
  .find(v => v.latest === true);
console.log(latest.version_name); // "40.2.2"
```

### Filter by Series
```javascript
const series32 = data.tiktok_version_database.versions
  .filter(v => v.series === "32.x");
```

### Get Version by Code
```javascript
const version = data.tiktok_version_database.versions
  .find(v => v.version_code === "402020");
```

## Why This Exists

TikTok version tracking is surprisingly complex. Official sources are scattered, version codes follow non-standard patterns, and release dates vary across platforms. This database consolidates everything into a single, reliable source.

**Use cases:**
- App compatibility testing
- Security research and vulnerability tracking
- Analytics and usage statistics
- Automated deployment pipelines
- Version comparison tools

## Data Quality

- **Source**: APK Mirror (official Android APK repository)
- **Verification**: Manual verification of release dates and version codes
- **Exclusions**: Beta builds, TikTok Lite, and TikTok Studio variants
- **Format**: Standardized version code format (XXYYZZ)
- **Updates**: Regular updates as new versions are released

## Technical Notes

- Version codes follow TikTok's internal format
- Manifest codes include year prefix (YYYY + version_code)
- All dates in ISO format (YYYY-MM-DD)
- JSON validated and minified for production use

## License

This data is compiled from publicly available sources and is provided as-is for research and development purposes.

---

**Latest Update**: June 3, 2025  
**Current Version**: 40.2.2  
**Total Versions**: 90