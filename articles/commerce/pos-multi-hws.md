---
title: Vyhrazené platební terminály a výzvy pro tiskárnu a zásuvku s hotovostí
description: Tento článek poskytuje informace o možnosti mít vyhrazený platební terminál a vyzvat uživatele, aby vybral zásuvku s hotovostí a tiskárnu s účtenkami.
author: BrianShook
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 7c010448e43bbfb1f949508ce1b62bd07f3107e1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874914"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>Vyhrazené platební terminály a výzvy pro tiskárnu a zásuvku s hotovostí

[!include [banner](includes/banner.md)]

Tento článek poskytuje informace o možnosti mít vyhrazený platební terminál a vyzvat uživatele, aby vybral zásuvku s hotovostí a tiskárnu s účtenkami.

## <a name="overview"></a>Přehled

Moderní maloobchodníci hledají způsoby, jak zefektivnit pokladnu v obchodě. Současné trendy směrem k bezpapírové pokladně prostřednictvím elektronických plateb pomáhají nejen zajistit plynulejší nákupní prostředí, ale také redukují potřebu mít k dispozici plnou škálu periferních zařízení pro každého obchodníka.

Microsoft Dynamics 365 Commerce podporuje tyto trendy tím, že umožňuje scénář, kde má zařízení na pokladním místě (POS) vždy vyhrazený platební terminál, ale nemá vlastní tiskárnu účtenek nebo zásuvku s hotovostí. Když společníci musí vytisknout účtenku nebo provést platbu v hotovosti, jsou vyzváni k výběru hardwarové stanice, kde jsou tato zařízení nakonfigurována.

## <a name="key-terms"></a>Klíčové podmínky

| Termín | popis |
|---|---|
| Registrovat | Entita, která se používá ke konfiguraci instance registru POS. |
| Zařízení | Reprezentace fyzické instance registru POS a aplikace Moderní POS, která je k němu přiřazena. |
| Vyhrazená hardwarová stanice | Obchodní logika hadwarové stanice, která je součástí aplikací Modern POS for Windows a Modern POS for Android. |
| Port pro spouštění zásuvky (d/k) | Tradiční metoda pro připojení zásuvky k tiskárně účtenek. |
| Síťová příslušenství | Zabudovaná podpora pro síťové platební terminály, tiskárny účtenek a zásuvky na hotovost. |

## <a name="supported-pos-clients-and-devices"></a>Podporovaní klienti a zařízení POS

Funkce popsaná v tomto článku je podporována klienty Modern POS for Windows a Modern POS for Android POS.

Tato funkce podporuje síťové platební terminály a tiskárny účtenek. Podporu zásuvky můžete poskytnout připojením zásuvky k tiskárně účtenek prostřednictvím portu d/k.

Přímou podporu této funkce zajišťuje [Konektor plateb Dynamics 365 pro Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3). Jiné platební konektory však mohou být pro platby podporovány prostřednictvím sady Commerce software Development Kit (SDK). K podporovaným tiskárnám účtenek patří tiskárny účtenek od společnosti Star Micronics a Epson.

Pokud chcete nastavit tiskárny účtenek Star Micronics, nakonfigurujte zařízení pomocí obslužného programu tiskárny Star Micronics tak, aby ho bylo možné používat v síti. Tento nástroj také poskytuje IP adresu zařízení.

Pokud nastavujete tiskárny účtenek Epson, použijte obslužný program ePOS-Print k nastavení zařízení tak, aby používalo síťové protokoly.

Další informace o nastavení síťových periferních zařízení naleznete v části [Přehled podpory periferních zařízení sítě](./dev-itpro/network-peripherals.md).

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>Nastavení vyhrazeného platebního terminálu a výzva pro tiskárnu a zásuvku na hotovost

### <a name="set-up-hardware-profiles"></a>Nastavení profilů hardwaru

Musíte mít dva typy hardwarového profilu. První je přiřazen k registru. Druhý je přiřazen hardwarové stanici na úrovni obchodu a používá se k logickému seskupení tiskáren síťových účtenek a zásuvek na hotovost.

#### <a name="set-up-a-hardware-profile-for-the-register"></a>Nastavení hardwarového profilu registru

Chcete-li nastavit hardwarový profil přiřazený k registru, postupujte následovně.

1. V Dynamics 365 Commerce, vyhledejte **Hardwarový profil**.
2. Zvolte **Nové**.
3. Přiřaďte číslo hardwarového profilu a zadejte popis. Tento hardwarový profil bude přiřazen k samotnému registru. Proto bude stačit popis jako **Vyhrazeno se zálohou**.
4. Na pevné záložce pro různé typy zařízení nastavte následující typy zařízení.

    | Zařízení | Typ | Název zařízení | Další údaje |
    |---|---|---|---|
    | Tiskárna | Síť | *Libovolná* | U názvu zařízení je rozlišována velikost písmen. **ID profilu účtenky** by mělo být stejné jako **ID profilu účtenky**, které je mapováno na síťovou tiskárnu nastavenou v hardwarovém profilu, který je přiřazen hardwarové stanici na úrovni kanálu. |
    | Zásuvka s hotovostí | Síť | *Libovolná* | U názvu zařízení je rozlišována velikost písmen. Nastavte hodnotu možnosti **Použít sdílenou směnu** na **Ano**. |
    | Služba EFT | Adyen | Nelze použít | Informace o nastavení předem integrovaného konektoru plateb Adyen pro online obchody naleznete v tématu [Konektor plateb Dynamics 365 pro Ayden](./dev-itpro/adyen-connector.md?tabs=8-1-3) Jiné platební konektory však mohou být pro platby podporovány prostřednictvím sady [Commerce software development kit (SDK) pro platby](./dev-itpro/end-to-end-payment-extension.md). |
    | Klávesnice pro kód PIN | Síť | **MicrosoftAdyenDeviceV001** | Žádný. |

5. V Dynamics 365 Commerce vyhledejte **Registry**.
6. Vyberte registr výběrem čísla registru a poté vyberte **Upravit**.
7. Přiřaďte hardwarový profil, který jste právě vytvořili, registru, který by měl používat vyhrazený platební terminál. Zařízení, které je mapováno do tohoto registru, musí používat aplikaci Modern POS for Windows nebo Modern POS for Android.
8. Zvolte **Uložit**.
9. V podokně akcí na kartě **Registry** zvolte **Konfigurovat IP adresy**.
10. Na pevné záložce **Podložka PIN** zadejte IP adresu platebního terminálu. Informace o tom, jak získat adresu IP platebního terminálu pomocí konektoru Adyen, naleznete v části [Platební konektor Dynamics 365 pro Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3).
11. Zvolte **Uložit**.

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>Nastavení hardwarového profilu pro tiskárnu účtenek a zásuvku na hotovost

Chcete-li nastavit hardwarový profil, který se používá k seskupení síťové tiskárny a zásuvky na hotovost, postupujte takto.

1. V Dynamics 365 Commerce, vyhledejte **Hardwarový profil**.
2. Zvolte **Nové**.
3. Přiřaďte číslo hardwarového profilu a zadejte popis. Tento hardwarový profil bude použit pro seskupení účtenky a zásuvky na hotovost. Proto bude stačit popis, jako je **Síťová tiskárna a zásuvka na hotovost**.
4. Na pevné záložce pro různé typy zařízení nastavte následující typy zařízení.

    | Zařízení | Typ | popis | Další údaje |
    |---|---|---|---|
    | Tiskárna | Síť | **Epson** nebo **Star** | U názvu zařízení je rozlišována velikost písmen. **ID profilu účtenky** by mělo být stejné jako **ID profilu účtenky**, které je namapováno na síťovou tiskárnu nastavenou v hardwarovém profilu, který je přiřazen k registru. |
    | Zásuvka s hotovostí | Záloha | **Epson** nebo **Star** | U názvu zařízení je rozlišována velikost písmen. nastavte hodnotu možnosti **Použít sdílenou směnu** na **Ano**. |

5. Zvolte **Uložit**.

### <a name="set-up-hardware-stations"></a>Nastavení hardwarových stanic

Musíte mít dvě hardwarové stanice. První bude mapována do registru. Druhá bude vybrána podle potřeby, kdykoli je třeba vytisknout účtenku nebo otevřít zásuvku na hotovost.

#### <a name="register-a-hardware-station"></a>Registrace hardwarové stanice

1. V Dynamics 365 Commerce vyhledejte **Všechny obchody**.
2. Vyberte obchod výběrem jeho hodnot **ID maloobchodního kanálu** a poté vyberte **Upravit**.
3. Na pevné záložce **Hardwarové stanice** vyberte **Přidat**.
4. Nastavte pole **Typ hardwarové stanice** na **Vyhrazená**.
5. Zadejte popis, ale nenastavujte žádné další hodnoty pro tuto hardwarovou stanici. Tato hardwarová stanice bude vždy použita pro registr. 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>Nastavení hardwarové stanice pro tiskárnu účtenek a zásuvku na hotovost

1. V Dynamics 365 Commerce vyhledejte **Všechny obchody**.
2. Vyberte obchod výběrem jeho hodnot **ID maloobchodního kanálu** a poté vyberte **Upravit**.
3. Na pevné záložce **Hardwarové stanice** vyberte **Přidat**.
4. Nastavte pole **Typ hardwarové stanice** na **Vyhrazená**.
5. Zadejte popis. Tato hardwarová stanice bude použita pro seskupení účtenky a zásuvky na hotovost.
6. V poli **Hardwarový profil** vyberte hardwarový profil, který jste dříve vytvořili pro tiskárnu účtenek a zásuvku na hotovost.
7. Zvolte **Uložit**.
8. Zatímco je stále vybrána hardwarová stanice pro tiskárnu účtenek a zásuvku na hotovost, vyberte **Konfigurovat IP adresy**.
9. Získejte IP adresu tiskárny a zadejte ji jako IP adresu pro tiskárnu účtenek i zásuvky na hotovost.
10. Zvolte **Uložit**
11. Vyhledejte **Plány distribuce**.
12. Vyberte plán distribuce **1090** a poté vyberte možnost **Spustit**.
13. Vyberte plán distribuce **1070** a poté vyberte možnost **Spustit**.

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>Nastavte systém tak, aby vyžadoval výběr tiskárny a zásuvky na hotovost podle potřeby

1. V podporovaném klientovi POS zavřete aktuální směnu, pokud je směna otevřená.
2. Přihlaste se a poté vyberte **Operace zásuvky mimo zásuvku**.
3. Použijte operaci **Správa hardwarových stanic** pro zapnutí hardwarové stanice.
4. Vyberte hardwarovou stanici, kterou jste pro registr vytvořili, a aktivujte ji.
5. Odhlaste se ze systému POS a otevřete směnu.

Platební terminál, který je přiřazen k hardwarovému profilu, bude nyní vždy aktivní a budete vyzváni, pokud bude požadována tiskárna s účtenkou nebo zásuvka na hotovost.

Mnoho obchodníků, kteří o tuto funkci požádali, má zájem omezit plýtvání poskytováním e-mailových účtenek a podporou elektronických plateb. V závislosti na konfiguraci POS jsou obchodní partneři vyzváni k výběru tiskárny účtenek nebo zásuvky na hotovost, pouze pokud zákazník chce fyzickou účtenku nebo chce platit v hotovosti.

Zaměstnanci obchodu jsou vyzváni, aby vybrali hardwarovou stanici pouze jednou pro každou transakci, pakliže není nutné vytisknout účtenku a použít peníze k platbě, ale původně vybraný hardwarový profil nezahrnuje obě zařízení. V takovém případě bude přidružený obchod vyzván znovu k výběru hardwarové stanice, kterou lze použít k dokončení transakce.

## <a name="related-articles"></a>Související články

- [Nastavení hybridní aplikace POS v systému Android a iOS](./dev-itpro/hybridapp.md)
- [Platební konektor Dynamics 365 pro Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3)
- [Přehled podpory periferní sítě](./dev-itpro/network-peripherals.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
