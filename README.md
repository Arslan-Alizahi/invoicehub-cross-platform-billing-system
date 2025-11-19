# InvoiceHub

A cross-platform business management application built with .NET MAUI Blazor Hybrid. Manage your inventory, create professional invoices, track stock levels, and export bills as PDF or images.

## Features

### Dashboard
- Quick overview of business statistics
- Total categories, products, bills, and pending payments
- Recent bills at a glance
- Quick action buttons for common tasks

### Inventory Management
- **Categories**: Organize products into categories
- **Products**: Complete product management with:
  - Name, price, and company details
  - Power rating and electrical specifications
  - Stock quantity tracking
  - Minimum/maximum stock level alerts

### Billing System
- Create professional invoices with customer details
- Add multiple items to a single bill
- Apply discounts (percentage or fixed amount)
- Bill status tracking:
  - Quotation
  - Payment Pending
  - Paid
- Auto-generated bill numbers
- View and manage bill history

### Stock Management
- Real-time stock tracking
- Low stock alerts and notifications
- Automatic stock reduction on billing
- Minimum stock level warnings

### Export Options
- Export bills as **PDF** documents
- Export bills as **Images** (PNG)
- Professional invoice layout with company branding

## Tech Stack

- **Framework**: .NET 9.0 MAUI Blazor Hybrid
- **UI**: Blazor Components with Bootstrap CSS
- **Database**: SQLite with Entity Framework Core 9.0
- **Graphics**: SkiaSharp 2.88.8 for PDF/Image generation
- **Icons**: Font Awesome

## Supported Platforms

| Platform | Minimum Version |
|----------|----------------|
| Android | API 24 (Android 7.0) |
| iOS | 15.0 |
| macOS | 15.0 (Catalyst) |
| Windows | 10.0.17763 |

## Project Structure

```
src/SABES/
├── Components/
│   ├── Layout/
│   │   └── MainLayout.razor
│   └── Pages/
│       ├── Home.razor
│       ├── Categories.razor
│       ├── Items.razor
│       ├── Bills.razor
│       ├── BillDetails.razor
│       ├── Billing.razor
│       └── LowStock.razor
├── Data/
│   └── SabesDbContext.cs
├── Models/
│   ├── Bill.cs
│   ├── BillItem.cs
│   ├── Category.cs
│   └── Item.cs
├── Services/
│   ├── BillService.cs
│   ├── CategoryService.cs
│   ├── FileService.cs
│   └── ItemService.cs
├── Platforms/
│   ├── Android/
│   ├── iOS/
│   ├── MacCatalyst/
│   └── Windows/
├── Resources/
│   ├── AppIcon/
│   ├── Fonts/
│   ├── Images/
│   └── Splash/
└── wwwroot/
    └── css/
```

## Getting Started

### Prerequisites

- .NET 9.0 SDK
- Visual Studio 2022 (17.8+) with MAUI workload
- Platform-specific requirements:
  - **Android**: Android SDK API 24+
  - **iOS/macOS**: Xcode 15+ (Mac required)
  - **Windows**: Windows 10 SDK

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/InvoiceHub.git
cd InvoiceHub
```

2. Restore dependencies
```bash
dotnet restore
```

3. Build the project
```bash
dotnet build
```

### Running the Application

**Windows**
```bash
dotnet run --framework net9.0-windows10.0.19041.0
```

**Android**
```bash
dotnet run --framework net9.0-android
```

**iOS** (requires Mac)
```bash
dotnet run --framework net9.0-ios
```

**macOS** (requires Mac)
```bash
dotnet run --framework net9.0-maccatalyst
```

## Database

The application uses SQLite for local data storage. The database is automatically created on first run and includes:

- **Categories**: Product categories
- **Items**: Products with stock information
- **Bills**: Invoice records
- **BillItems**: Line items for each bill

## Building for Release

### Android APK
```bash
dotnet publish -f net9.0-android -c Release
```

### Windows
```bash
dotnet publish -f net9.0-windows10.0.19041.0 -c Release
```

### iOS/macOS
```bash
dotnet publish -f net9.0-ios -c Release
dotnet publish -f net9.0-maccatalyst -c Release
```

## Configuration

The application uses the following default settings:

- **App ID**: `com.arslandevs.sabes`
- **App Title**: SABES - Powered by Arslandevs
- **Version**: 1.0

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with [.NET MAUI](https://dotnet.microsoft.com/apps/maui)
- UI powered by [Blazor](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor)
- PDF/Image generation by [SkiaSharp](https://github.com/mono/SkiaSharp)
- Icons by [Font Awesome](https://fontawesome.com)

---

**Developed by Arslandevs | Powered by CodingZoo**
