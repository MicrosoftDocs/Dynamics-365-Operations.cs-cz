---
title: Přehled aplikace Dynamics 365 Payment Connector pro Adyen
description: Tento článek poskytuje přehled o platebním konektoru Microsoft Dynamics 365 pro Adyen.
author: rassadi
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.openlocfilehash: 58d88e023b73ce19331bd6f54644a62d8f6f35af
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812079"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Přehled aplikace Dynamics 365 Payment Connector pro Adyen

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled o platebním konektoru Microsoft Dynamics 365 pro Adyen a obsahuje úplný seznam podporovaných funkcí. Související články se týkají registrace Adyen, konfigurace konektoru, často kladených dotazů a pokynů pro řešení některých běžných problémů.

## <a name="key-terms"></a>Klíčové podmínky

| Termín | Popis |
|---|---|
| Konektor platby | Rozšíření, které usnadňuje komunikaci mezi Microsoft Dynamics 365 Commerce (a souvisejícími součástmi) a platební službu. Konektor, který je popsán v tomto článku, byl implementován pomocí standardní sady pro vývoj softwaru pro platby (SDK). |
| Karta je přítomna | Týká se platebních transakcí, při nichž je fyzická karta předložena a použita na platebním terminálu připojeném k pokladnímu místu Dynamics 365. |
| Karta není přítomna | Týká se platebních transakcí, kde není přítomna fyzická karta, jako jsou scénáře elektronického obchodu nebo call centra. V těchto scénářích se informace související s platbou zadávají ručně buď na webových stránkách elektronického obchodu, v telefonním centru, nebo na prodejním místě či platebním terminálu. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Podporované funkce, verze a terminály

Předem připravený platební konektor Dynamics 365 pro Adyen používá standardní SDK pro platby. Nemá proto speciální funkce, které nejsou dostupné také pro jiné platební konektory.

### <a name="supported-versions"></a>Podporované verze

#### <a name="microsoft-dynamics-365-supported-versions"></a>Podporované verze Microsoft Dynamics 365
První stranou připravený konektor plateb Dynamics 365 pro Adyen je podporován v Microsoft Dynamics 365 Finance verze 8.1.3 (leden 2019) nebo novější a v Microsoft Dynamics 365 Retail verze 8.1.3 nebo novější. Třetí strany však mohou stále vyvíjet další platební konektory pro Adyen pro starší verze Microsoft Dynamics 365.

#### <a name="supported-adyen-firmware-versions"></a>Podporované verze firmwaru Adyen

Níže uvedený seznam popisuje minimální a maximální verze firmwaru Adyen, které jsou podporovány pro jednotlivé verze Microsoft Dynamics 365 Retail POS.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail POS verze 10.0.25
| Minimální verze firmwaru Adyen | Maximální verze firmwaru Adyen |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail POS verze 10.0.26
| Minimální verze firmwaru Adyen | Maximální verze firmwaru Adyen |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail POS verze 10.0.27
| Minimální verze firmwaru Adyen | Maximální verze firmwaru Adyen |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail POS verze 10.0.28
| Minimální verze firmwaru Adyen | Maximální verze firmwaru Adyen |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail POS verze 10.0.29
| Minimální verze firmwaru Adyen | Maximální verze firmwaru Adyen |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail POS verze 10.0.30
| Minimální verze firmwaru Adyen | Maximální verze firmwaru Adyen |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Adyen může vydat aktualizace menších verzí poté, co Microsoft otestuje hlavní verzi. Dokud je podporována hlavní verze, je v pořádku mít menší verze v rámci stejné hlavní verze. Tyto aktualizace jsou obvykle velmi cílené opravy a nesplňují laťku pro úplné opětovné testování, pokud byla dříve testována stejná hlavní verze firmwaru. Aktualizace by neměly překročit maximální verzi firmwaru Adyen uvedenou v dokumentaci. 
>
> Migrace z verze firmwaru Adyen starší než verze 53 na verzi 53 vyžaduje POS KB **4577957** pro měsíční aktualizace Commerce, verze 10.0.11 až 10.0.14. Pokud se jedna z těchto verzí používá a neobsahuje opravu hotfix, po upgradu platebního terminálu umožní platby pouze prostřednictvím NFC. Použití opravy hotfix na POS tento problém vyřeší. Pokud je verze POS starší než verze 10.0.11, odešlete žádost o podporu s poznámkou, že oprava pro KB **4577957** je vyžadováno pro mimo provoz MPOS.
> 
> Pro verze firmwaru Adyen 59p7 až 62p9 **vyplacení dárkové karty** operace vyžaduje zadání PIN dvakrát ve scénářích, kdy se dárková karta zadává ručně. Tento problém se při protažení dárkové karty neopakuje. Adyen provádí šetření. 

### <a name="supported-payment-terminals"></a>Podporované platební terminály
Dynamics 365 Payment Connector for Adyen využívá výhody agnostiky zařízení [Rozhraní API platebního terminálu Ayden](https://www.adyen.com/blog/introducing-the-terminal-api). Podporuje všechny platební terminály, které toto aplikační programovací rozhraní (API) podporuje. Kompletní seznam podporovaných platebních terminálů najdete na stránce [POS terminály Adyen](https://www.adyen.com/pos-payments/terminals).

Následující video popisuje možnosti platebního terminálu Adyen Castles SE1 Android .


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bKeM]

### <a name="supported-payment-instruments"></a>Podporované platební nástroje

#### <a name="supported-debit-and-credit-cards"></a>Podporované debetní a kreditní karty

| Značka | Varianta | Karta je přítomna | Elektronický obchod | Kontaktní středisko |
|---|---|:-:|:-:|:-:|
| MasterCard | Kredit | ✔ | ✔ | ✔ |
| MasterCard | Debet | ✔ | ✔ | ✔ |
| MasterCard | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| MasterCard | Apple Pay | ✔ |  |  |
| MasterCard | Samsung Pay | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Maestro Samsung Pay | ✔ |  |  |
| MasterCard | Maestro UK | ✔ | ✔ | ✔ |
| VISA | Kredit | ✔ | ✔ | ✔ |
| VISA | Debet | ✔ | ✔ | ✔ |
| VISA | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| VISA | Android Pay | ✔ |  |  |
| VISA | Apple Pay | ✔ |  |  |
| VISA | Samsung Pay | ✔ |  |  |
| VISA | VISA Checkout | ✔ | ✔ | ✔ |
| VISA | VISA Dankort | ✔ | ✔ | ✔ |
| VISA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VISA | Karta VISA Aravia | ✔ | ✔ | ✔ |
| AMEX | Kredit | ✔ | ✔ | ✔ |
| AMEX | Debet | ✔ | ✔ | ✔ |
| AMEX | Android Pay | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Pay | ✔ |  |  |
| AMEX | AMEX Commercial | ✔ | ✔ | ✔ |
| AMEX | AMEX Consumer | ✔ | ✔ | ✔ |
| AMEX | AMEX Corporate | ✔ | ✔ | ✔ |
| AMEX | AMEX Small Business | ✔ | ✔ | ✔ |
| Zjistit | Standardní | ✔ | ✔ | ✔ |
| Zjistit | Android Pay | ✔ |  |  |
| Zjistit | Apple Pay | ✔ |  |  |
| Zjistit | Samsung Pay | ✔ |  |  |
| Diners   | Standardní | ✔ | ✔ | ✔ |
| Dineromail | Standardní | ✔ | ✔ | ✔ |
| JCB | Standardní | ✔ | ✔ | ✔ |
| Union Pay\* | Standardní | ✔ |  |  |
| Interac Debit\* | Standardní | ✔ |  |  |

\*Tokeny opakujících se karet Interac a Union Pay nejsou společností Adyen poskytovány, takže je nelze podporovat pro transakce bez karty.

#### <a name="supported-gift-cards"></a>Podporované dárkové karty
| Schéma | Karta je přítomna | Karta není přítomna |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

Chcete-li podporovat tato externí schémata dárkových karet prostřednictvím platebního konektoru Dynamics 365 pro Adyen, musíte provést další kroky. Více informací viz [Podpora externích dárkových karet](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>Podporované peněženky

| Schéma | Karta je přítomna | Karta není přítomna |
|---|---|---|
| Alipay | Podpora bude přidána v budoucí verzi. | Číslo |
| WeChat | Podpora bude přidána v budoucí verzi. | Číslo |

#### <a name="supported-card-present-input-methods"></a>Podporovaná karta obsahuje vstupní metody
| Vstupní metoda | Podporováno | Poznámky |
|---|:-:|---|
| Klesnutí | ✔ | |
| Protáhnout | ✔ | |
| Klepněte | ✔ | |
| Ruční vstup přes POS UI. |  | Momentálně nepodporováno |
| Manuální zadání prostřednictvím platebního terminálu. | ✔ | Podporuje ruční zadávání kreditních, debetních a dárkových karet se zadáním kódu PIN. | 


#### <a name="supported-card-present-countries"></a>Země, kde je karta podporována

V následujících zemích jsou k dispozici komponenty Commerce a karta poskytuje podporu od společnosti Adyen. Pro aktuální mezinárodní dostupnost Commerce navštivte [stránku mezinárodní dostupnosti](/dynamics365/get-started/availability).

| Země | Podporováno |
| --- | :-: |
| Austrálie | ✔ |
| Rakousko | ✔ |
| Belgie | ✔ |
| Kanada | ✔ |
| Česká republika | ✔ |
| Dánsko | ✔ |
| Estonsko | ✔ |
| Finsko | ✔ |
| Francie | ✔ |
| Německo | ✔ |
| Hongkong | ✔ |
| Maďarsko | ✔ |
| Island | ✔ |
| Irsko | ✔ |
| Itálie | ✔ |
| Japonsko | Budoucí vydání |
| Lotyšsko | ✔ |
| Litva | ✔ |
| Malajsie | ✔ |
| Nizozemsko | ✔ |
| Nový Zéland | ✔ |
| Norsko | ✔ |
| Polsko | ✔ |
| Singapur | ✔ |
| Švýcarsko | ✔ |
| Španělsko | ✔ |
| Švédsko | ✔ |
| Švýcarsko | ✔ |
| Spojené království | ✔ |
| Spojené státy | ✔ |
| Brazílie | Budoucí vydání |

#### <a name="supported-card-not-present-countries"></a>Podporované země, kde není karta k dispozici

Společnost Adyen podporuje transakce bez karty v následujících zemích. [Kontaktujte Adyen](https://www.adyen.com/contact/sales) pro podrobnosti o podpoře pro konkrétní zemi. Pro aktuální mezinárodní dostupnost Commerce navštivte [stránku mezinárodní dostupnosti](/dynamics365/get-started/availability).

| Země | 
| --- |
| Argentina |
| Arménie |
| Austrálie |
| Rakousko |
| Bahrajn |
| Belgie |
| Brazílie |
| Bulharsko |
| Kanada |
| Chile |
| Čína |
| Kolumbie |
| Chorvatsko |
| Kypr |
| Česká republika  |
| Dánsko |
| Egypt |
| Estonsko |
| Finsko |
| Francie |
| Gruzie |
| Německo |
| Gibraltar |
| Řecko |
| Guernsey |
| Hongkong |
| Maďarsko |
| Island |
| Indie |
| Indonésie |
| Irsko |
| Ostrov Man |
| Izrael |
| Itálie |
| Japonsko |
| Jersey |
| Korea |
| Kuvajt |
| Lotyšsko |
| Litva |
| Lucembursko |
| Malajsie |
| Malta |
| Mexiko |
| Maroko |
| Nizozemsko |
| Nový Zéland |
| Norsko |
| Peru |
| Polsko |
| Portugalsko |
| Katar |
| Rumunsko |
| Saúdskoarabské království |
| Srbsko |
| Singapur |
| Slovensko |
| Slovinsko |
| Jižní Afrika |
| Španělsko |
| Švédsko |
| Švýcarsko |
| Tchaj-wan |
| Tanzánie |
| Thajsko |
| Turecko |
| Spojené arabské emiráty (UAE) |
| Spojené království |
| Spojené státy americké včetně Portorika  |

#### <a name="supported-dynamics-365-payment-features"></a>Podporované platební funkce Dynamics 365

Následující tabulka ukazuje sadu funkcí, které platební konektor Dynamics 365 pro Adyen podporuje. Tyto funkce využívají vylepšení, která byla představena v sadě Payments SDK a některých komponentách v prosinci 2018. Nejsou exkluzivní pro Dynamics 365 Payment Connector pro Adyen. Další informace o tom, jak tato vylepšení využít pro jiný platební konektor, naleznete v části [Vytvoření koncové integrace plateb pro platební terminál](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| Schéma | Karta je přítomna | Karta není přítomna |
|---|:-:|:-:|
| [Vyplacení zůstatku dárkové karty](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Ochrana duplicitních plateb](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Tokenizace omnikanálu | ✔ | ✔ |
| Propojené refundace | ✔<br>(Počínaje 10.0.1) | ✔<br>(Počínaje 10.0.1) |
| [Ukládání online plateb](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(Počínaje 10.0.2) | 
| [Externí dárkové karty pro call centrum a elektronické obchodování](./gift-card.md) | ✔<br>(Počínaje 10.0.10) | 
| [Přesměrování platby SCA](../adyen_redirect.md) | | ✔<br>(Počínaje 10.0.12) |
| [Vyhrazené platební terminály a výzvy pro tiskárnu a zásuvku s hotovostí](../pos-multi-hws.md) | ✔<br>(Počínaje 10.0.12) | |
| [Podpora spropitného na úrovni SDK prostřednictvím konektoru Adyen](tipping.md) | ✔<br>(Počínaje 10.0.14) | |
| [Přírůstkové zachycení pro fakturaci objednávky](incremental-capture.md) |  | ✔<br>(Počínaje 10.0.18) |
| [Platby Wallet](../wallets.md) |  | ✔<br>(Počínaje 10.0.20) |
| [Google Pay s Adyen](google-pay-adyen.md) |  | ✔<br>(Počínaje 10.0.27) |

## <a name="next-steps"></a>Další kroky

Informace o registraci a konfiguraci platebního konektoru Dynamics 365 pro Adyen naleznete v části [Nastavení platebního konektoru Dynamics 365 pro Adyen](adyen-connector-setup.md).

## <a name="additional-resources"></a>Další prostředky

[Nastavení aplikace Dynamics 365 Payment Connector pro Adyen](adyen-connector-setup.md)

[Časté otázky o aplikaci Dynamics 365 Payment Connector pro Adyen](adyen-connector-faq.md)

[Odstranění potíží s aplikací Dynamics 365 Payment Connector pro Adyen](adyen-connector-troubleshoot.md)

[Časté dotazy k platbám](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
