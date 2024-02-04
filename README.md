# PinguApps.Blazor.QRCode
A Blazor component for generating QR codes. This component encodes specified data into a QR code image, which can be customized in terms of size, colors, and error correction level. The QR code is generated as an SVG for optimal scalability and clarity.

[![NuGet Version](https://img.shields.io/nuget/v/PinguApps.Blazor.QRCode?logo=nuget&style=for-the-badge)](https://www.nuget.org/packages/PinguApps.Blazor.QRCode) [![NuGet Downloads](https://img.shields.io/nuget/dt/PinguApps.Blazor.QRCode?style=for-the-badge&logo=nuget)](https://www.nuget.org/packages/PinguApps.Blazor.QRCode) ![GitHub License](https://img.shields.io/github/license/PinguApps/Blazor.QRCode?style=for-the-badge) [![GitHub Repo stars](https://img.shields.io/github/stars/PinguApps/Blazor.QRCode?style=for-the-badge&logo=github)](https://github.com/PinguApps/Blazor.QRCode)
<!-- [TODO: Build Status](https://shields.io/badges/git-hub-actions-workflow-status) -->

## 🌐 Demo 
Check out the QRCode component on the [demo site](https://pinguapps.github.io/Blazor.QRCode/)!

## 🔧 Installation
To install the package, you can either install with the following command:
`Install-Package PinguApps.Blazor.QRCode`
Or you can search in the Nuget package manager for `PinguApps.Blazor.QRCode`.

## 🚀 Usage

Once the package is installed, you will want to add the following statement to your `_Imports.razor`:
```razor
@using PinguApps.Blazor.QRCode
```

Now you can simply use the component:
```razor
<QRCode Data="My Data!" Size="150px" />
```

### 🟣 Parameters

| Parameter Name | Type | Required? | Description | Default Value | Possible Values |
|:--:|:--:|:--:|:--:|:--:|:--:|
| Data | String | ❌ | The data to be encoded into the QR code. | `string.Empty` |  |
| ErrorCorrection | ErrorCorrection | ❌ | Sets the error correction level for the QR code, which enables it to be decoded even if partially damaged or obscured. | `ErrorCorrection.Low` | `ErrorCorrection.Low`<br>`ErrorCorrection.Medium`<br>`ErrorCorrection.Quartile`<br>`ErrorCorrection.High` |
| Size | String | ❌ | Sets the width and height of the generated SVG. | 100% | Any valid html size for width & height |
| PaddingCells | Int | ❌ | The number of empty cells as padding around the QR code. | 1 |  |
| ForeColor | String | ❌ | Sets the foreground color of the QR code. | #000000 | Any valid html color |
| BackColor | String | ❌ | Sets the background color of the QR code. | #ffffff | Any valid html color |
| AriaDescription | String | ❌ | Provides an accessible description for the QR code, enhancing usability for screen reader users. This description is used as the aria-label attribute value of the QR code's SVG element, offering context or details about the QR code's content or purpose. | QR Code |  |
| Class | String? | ❌ | Optional CSS class to be applied to the QR code. | `null` |  |
| Id | String? | ❌ | Optional ID to be applied to the QR code. | `null` |  |

## ✅ Features
- **JavaScript-Free**: No dependency on JavaScript, ensuring full functionality even in environments where JavaScript is disabled or not supported.
- **Static SSR & Prerendering Compatibility**: Seamlessly works with static SSR (Server-Side Rendering) and prerendering scenarios, making it suitable for the static SSR pages of the new .NET Identity template as a 2FA QR code generator.
- **Adjustable Error Correction**: Allows setting the error correction level (Low, Medium, Quartile, High) to make the QR code decodable even when partially damaged or obscured.
- **Dynamic Data Encoding**: Capable of encoding provided string data into the QR code, facilitating versatile usage scenarios.
- **Customizable Size**: Supports setting the width and height of the generated SVG QR code, with a default of "100%" for flexible integration into various UI designs.
- **Configurable Padding**: Allows specifying the number of empty cells as padding around the QR code to adjust its appearance, with a default setting of 1.
- **Foreground and Background Color Customization**: Offers options to set the foreground and background colors of the QR code, defaulting to black (#000000) and white (#ffffff), respectively.
- **Accessibility Support**: Enhances usability for screen reader users with an accessible description for the QR code, which is used as the `aria-label` attribute value of the SVG element.
- **Styling Options**: Supports optional CSS class and ID attributes for the QR code, enabling further customization and styling flexibility.
