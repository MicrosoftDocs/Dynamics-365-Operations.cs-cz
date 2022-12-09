---
title: Aplikace Store Commerce pro mobilní platformy
description: Tento článek popisuje, jak začít používat aplikaci Microsoft Dynamics 365 Commerce Store Commerce pro Android a iOS.
author: stuharg
ms.date: 11/30/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: dc952698a2a3301aff312e8310c58cbbb9cfe290
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815776"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>Aplikace Store Commerce pro mobilní platformy

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tento článek popisuje, jak začít používat aplikace Microsoft Dynamics 365 Commerce Store Commerce pro Android a iOS.

Mobilní aplikace Dynamics 365 Commerce pro Android a iOS zrychlují a zjednodušují proces nasazení plnohodnotných mobilních pokladních míst (POS) pro vaše maloobchodní prostředí. Mobilní aplikace Store Commerce poskytují téměř všechny možnosti a výhody [aplikace Store Commerce pro Windows](store-commerce.md) a fungují dobře na široké škále telefonů a tabletů iOS a Android. Mobilní aplikace Store Commerce lze nainstalovat přímo z obchodů s aplikacemi Apple a Google Play a pro jejich nasazení nebo aktualizaci není nutné, aby vývojář vytvořil nový balíček aplikace. 

Mobilní aplikace Store Commerce si zachovávají plnou funkční paritu se současnými hybridními aplikacemi pro maloobchod. Store Commerce pro iOS navíc zahrnuje podporu pro vyhrazenou hardwarovou stanici, takže zařízení iOS mohou komunikovat se síťovými platebními terminály, tiskárnami účtenek a pokladními zásuvkami bez nutnosti nasazení sdílené hardwarové stanice. 

> [!IMPORTANT]
> Aplikace Store Commerce pro Windows, Android a iOS jsou další generací POS aplikací pro Dynamics 365 Commerce. Aplikace Store Commerce nabízejí četná vylepšení oproti svým předchůdcům, přičemž si zachovávají plnou funkčnost a paritu funkcí. Společnost Microsoft ukončí podporu MPOS a hybridní aplikace Android a iOS Retail POS koncem roku 2023 a doporučuje, abyste pro všechna nová nasazení POS používali Store Commerce nebo Cloud POS (CPOS). Stávající zákazníci by měli plánovat migraci z maloobchodní hybridní aplikace na Store Commerce. Další informace najdete v části [Migrace moderního POS do Store Commerce](pos-extension/migrate-mpos-store-commerce.md). 

## <a name="app-architecture"></a>Architektura aplikace

Mobilní aplikace Store Commerce používají stejnou topologii jako aplikace Store Commerce pro Windows, když jsou nasazeny v hybridním režimu. Mobilní aplikace Store Commerce jsou shellové aplikace, které vykreslují CPOS přímo z Commerce Scale Unit (CSU) a připojují se k bezobslužné Commerce a Commerce headquarters prostřednictvím CSU. Model shellové aplikace umožňuje aplikacím Store Commerce podporovat vyhrazenou hardwarovou stanici pro přímou integraci s platebním terminálem, tiskárnou, zásuvkou na peníze a dalšími periferiemi. Chcete-li používat hardwarová zařízení, nemusíte nastavovat sdílenou hardwarovou stanici. 

Chcete-li aktualizovat mobilní aplikaci Store Commerce, stačí aktualizovat CSU. Všechny nové funkce POS budou automaticky vyzvednuty aplikací. Další informace o tom, jak aktualizovat CSU, najdete v článku [Použití aktualizací a rozšíření na Commerce Scale Unit (cloud)](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md).

Shellové aplikace jsou obsluhovány prostřednictvím aktualizací obchodu s aplikacemi. Když vedlejší verze dosáhne obecné dostupnosti (GA), Microsoft ji zveřejní v obchodech s aplikacemi. Společnost Microsoft může také publikovat opravy mezi aktualizacemi menších verzí, aby uvolnila opravy chyb s vysokou prioritou.

## <a name="prerequisites"></a>Předpoklady

Mobilní aplikace Store Commerce vyžadují Dynamics 365 Commerce, konkrétně Commerce headquarters a součásti CSU. V následující tabulce jsou uvedeny minimální verze operačního systému (OS) a CSU, které vyžadují mobilní aplikace pro Android a iOS. 

| Předpoklad | Android      | iOS  |
| ------------ | ------------ | ---- |
| Verze operačního systému   | 7.0          | 15.0 |
| Verze CSU  | 9.38.22266.8 | Bude určeno  |

## <a name="install-the-app"></a>Instalace aplikace

Mobilní aplikace Store Commerce můžete nainstalovat přímo z obchodu Google Play nebo Apple App Store. 

- [Aplikace Store Commerce pro Android](https://aka.ms/storecommerceandroid)
- [Aplikace Store Commerce pro iOS](https://aka.ms/storecommerceios)

Balíčky aplikací Android (.apk) a Apple (.ipa) lze také stáhnout z knihovny sdíleného majetku v Microsoft Dynamics Lifecycle Services. 

## <a name="device-and-register-setup"></a>Nastavení registrační pokladny a zařízení

Než bude možné aktivovat registrační pokladnu v mobilních aplikacích Store Commerce, musíte nastavit zařízení a pokladnu v Commerce headquarters. Další informace naleznete v tématu [Zařízení a registrační pokladny](../implementation-considerations-devices.md). 

### <a name="device-setup"></a>Nastavení zařízení

Chcete-li vytvořit a nastavit nové zařízení, postupujte podle těchto kroků.

1. V Commerce headquarters přejděte na možnost **Maloobchod a obchod \> Nastavení kanálu \> Nastavení POS \> Zařízení**. 
1. Vytvořte nové zařízení a vyberte buď **Modern POS - Android** nebo **Modern POS - iOS** jako typ aplikace v závislosti na mobilní aplikaci, kterou nasazujete. 

    > [!NOTE] 
    > Typy aplikací **Modern POS - Android** a **Modern POS - iOS** se také používají k nasazení současných hybridních aplikací pro Android a iOS. Po ukončení podpory MPOS budou popisky pro tyto typy aplikací aktualizovány na **Store Commerce - Android** a **Modern POS - iOS**. 

### <a name="register-setup"></a>Nastavení registrační poklady

Můžete vytvořit novou registrační pokladnu a přiřadit ji k zařízení, které jste vytvořili, nebo můžete k novému zařízení přiřadit existující registrační pokladnu. Více informací o registrech najdete v článku [Vytvoření a přidružení pokladen](../tasks/create-associate-registers.md).

### <a name="screen-layout-setup"></a>Nastavení rozložení obrazovky

Pokud měníte rozložení obrazovky, které je zahrnuto v ukázkových datech dodaných s vaší licencí Dynamics 365 Commerce, aplikace Store Commerce automaticky vybere zahrnuté kompaktní rozložení, pokud je rozlišení obrazovky vašeho zařízení menší než 480 &times; 853 pixelů v orientaci na výšku. Pokud však vytváříte rozložení obrazovky od začátku nebo pokud vaše mobilní zařízení používá větší rozlišení, než jaké podporuje kompaktní rozvržení, ujistěte se, že vytvoříte rozlišení a přidružené mřížky tlačítek, které jsou vhodné pro telefon nebo tablet, na který chcete rozložení nasadit. Další informace o konfiguracích rozložení obrazovky najdete v článku [Vizuální konfigurace uživatelského rozhraní POS](../pos-screen-layouts.md). 

Po konfiguraci zařízení a registračních pokladen přejděte v Commerce headquarters na stránku **Maloobchod a obchod \> Maloobchodní a obchodní ID \> Distribuční plány** a spusťte úlohu registrační pokladny.

## <a name="activate-a-device"></a>Aktivace zařízení

Chcete-li aktivovat zařízení v mobilní aplikaci Store Commerce, postupujte takto.

1. Otevřete aplikaci na mobilním zařízení.
1. Zadejte adresu URL CPOS, kterou najdete na stránce s podrobnostmi o prostředí ve službách Lifecycle Services nebo ve stránce **Profily kanálů** v Commerce headquarters (**Maloobchod a obchod \> Nastavení kanálu \> Profily kanálů**).
1. Přihlaste se pomocí přihlašovacích údajů pracovníka, který má oprávnění ke správě zařízení.
1. Vyberte obchod, který je přidružen k registrační pokladně, kterou jste vytvořili nebo znovu použili v Commerce headquarters.
1. Vyberte registrační pokladnu přidruženou k zařízení, které jste vytvořili v Commerce headquarters.
1. Vaše zařízení by nyní mělo být aktivováno. Do registrační pokladny se můžete přihlásit pomocí ID operátora a hesla pracovníka, který je přidružen k vámi vybranému obchodu. 

Další informace o aktivaci zařízení najdete v článku [Aktivace zařízení pokladního místa (POS)](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation).

## <a name="feature-parity-with-store-commerce-for-windows"></a>Parita funkcí se Store Commerce pro Windows

Následující tabulka porovnává schopnosti aplikace Store Commerce na platformách Windows, Android a iOS.

| Funkce                                                                               | Windows | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| Vyhrazená hardwarová stanice                                                            | Ano     | Ano     | Ano |
| Sdílená hardwarová stanice                                                               | Ano     | Ano     | Ano |
| Komunikace se síťovými periferiemi (platební terminál, tiskárna a pokladní zásuvka) | Ano     | Ano     | Ano |
| OLE pro periferní zařízení pokladního místa (OPOS) prostřednictvím místní hardwarové stanice             | Ano     | Číslo      | Číslo  |
| Offline režim                                                                          | Ano     | Číslo      | Číslo  |

## <a name="additional-resources"></a>Další prostředky

[Aplikace Store Commerce](store-commerce.md)

[Výběr mezi Store Commerce a Cloud POS](../mpos-or-cpos.md)

[Odstraňování problémů s nastavením a instalací služby Store Commerce](../troubleshoot/store-commerce-setup-installation.md)
