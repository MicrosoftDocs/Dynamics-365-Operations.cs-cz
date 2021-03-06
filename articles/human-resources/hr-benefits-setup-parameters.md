---
title: Nastavení parametrů správy zaměstnaneckých výhod a samoobslužných parametrů zaměstnanců pro všechny společnosti
description: Konfigurace parametrů správy zaměstnaneckých výhod a samoobsluhy zaměstnanců v Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d668238378e41287c7a9f845ae3e67078fc7776a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058961"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a>Nastavení parametrů správy zaměstnaneckých výhod a samoobslužných parametrů zaměstnanců pro všechny společnosti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Před nastavením plánů zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources musíte konfigurovat parametry správy zaměstnaneckých výhod. Tyto parametry nastaví výchozí hodnoty, kódy důvodů a další možnosti. 

## <a name="configure-general-parameters"></a>Konfigurace všeobecných parametrů

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Sdílené parametry lidských zdrojů**.

2. Na kartě **Správa zaměstnaneckých výhod** zadejte hodnoty pro následující pole:

   | Pole | popis |
   | --- | --- |
   | **Země nebo oblast** | Pole **Země/oblast** určuje pořadí zobrazení PSČ / států. Vybraná země se v rozevíracím seznamu zobrazí jako první. |
   | **Kód důvodu registrace** | Vyberte výchozí kód důvodu, který má být použit při vytvoření plánů zaměstnanců při otevřeném zpracování registrace. |
   | **Kód důvodu zrušení** | Kód důvodu, který má být použit při zrušení plánu zaměstnaneckých výhod. V průběhu procesu stornování se zobrazí dialogové okno. Uživatelé jej mohou v případě potřeby změnit v okně **Kód důvodu zrušení**. |
   | **Znovu otevřít kód důvodu** | Kód důvodu, který má být použit při zrušení plánu zaměstnaneckých výhod, se znovu otevře. V průběhu procesu stornování se zobrazí dialogové okno. Uživatelé jej mohou v případě potřeby změnit v okně **Znovu otevřít kód důvodu zrušení**. | 
   | **Kód důvodu životní události** | Kód důvodu, který má být použit při výskytu životní události. |
   | **Kód důvodu změny sazby** | Kód důvodu, který má být použit při zrušení a opětovném otevření plánu zaměstnaneckých výhod během procesu aktualizace změny sazby. Informuje o tom, které záznamy byly změněny procesem aktualizace změny sazby. |
   | **Roční výplata zaměstnaneckých výhod** | Umožňuje nastavit a částku **Roční výplata benefitů** pro zaměstnance. Human Resources budou využívat částku **Roční výplata benefitů** při určování částek krytí, namísto pevné roční náhrady. |
   | **Nově přijatý zaměstnanec je způsobilý** | Určuje, zda mají nově přijatí zaměstnanci nárok na podporu. |
   | **Období registrace nového zaměstnance** | Časové období, kdy je povolena registrace nově přijatého zaměstnance.</br></br>**Poznámka**: Toto nastavení přepíše jakékoli období registrace nově přijatého zaměstnance, které je nastaveno pro pravidlo nároku na plán. |
   | **Výchozí frekvence plateb** | Výchozí frekvence výplaty, která se použije při přidávání nových pracovníků. |
   | **Životní události povoleny** | Povolí životní události. |
   | **Skrýt staré formuláře zaměstnaneckých výhod** | Umožňuje skrýt starší formuláře zaměstnaneckých výhod. |
   | **Ověření zaměstnanecké výhody** | Ověřovací text, který se má použít při rezervaci výhod samoobsluhy. |
   | **Automatický výběr pověřených osob** | Určuje, zda mají být automaticky zvoleni následníci a příjemci na základě jejich nároku na možnosti plánu. |

3. Zvolte **Uložit**.

## <a name="configure-employee-self-service-parameters"></a>Konfigurace parametrů samoobsluhy zaměstnance

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry lidských zdrojů**.

2. Na kartě **Správa zaměstnaneckých výhod** zadejte hodnoty pro následující pole:

   | Pole | popis |
   | --- | --- |
   | **Ověření zaměstnanecké výhody** | Ověřovací text, který se má použít při rezervaci výhod samoobsluhy. |
   | **Automatický výběr pověřených osob** | Určuje, zda mají být automaticky zvoleni následníci a příjemci na základě jejich nároku na možnosti plánu. |

3. Zvolte **Uložit**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]