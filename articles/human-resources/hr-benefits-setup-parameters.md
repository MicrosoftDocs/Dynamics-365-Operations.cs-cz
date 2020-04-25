---
title: Nastavení parametrů správy zaměstnaneckých výhod
description: Nakonfigurujte parametry pro správu zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d6d463df08b9ae68047f09316f19e98740a8441
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229756"
---
# <a name="set-benefits-management-parameters"></a>Nastavení parametrů správy zaměstnaneckých výhod

Před nastavením plánů pracovního volna v Microsoft Dynamics 365 Human Resources musíte konfigurovat parametry správy zaměstnaneckých výhod. Tyto parametry nastaví výchozí hodnoty, kódy důvodů a další možnosti.

## <a name="configure-general-parameters"></a>Konfigurace všeobecných parametrů

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry**.

2. Na kartě **Obecné** zadejte hodnoty pro následující pole:

   | Pole | Popis |
   | --- | --- |
   | **Země nebo oblast** | Pole **Země/oblast** určuje pořadí zobrazení PSČ / států. Vybraná země se v rozevíracím seznamu zobrazí jako první. |
   | **Kód důvodu registrace** | Vyberte výchozí kód důvodu, který má být použit při vytvoření plánů zaměstnanců při otevřeném zpracování registrace. |
   | **Kód důvodu zrušení** | Kód důvodu, který má být použit při zrušení plánu zaměstnaneckých výhod. V průběhu procesu stornování se zobrazí dialogové okno. Uživatelé jej mohou v případě potřeby změnit v okně **Kód důvodu zrušení**. |
   | **Znovu otevřít kód důvodu** | Kód důvodu, který má být použit při zrušení plánu zaměstnaneckých výhod, se znovu otevře. V průběhu procesu stornování se zobrazí dialogové okno. Uživatelé jej mohou v případě potřeby změnit v okně **Znovu otevřít kód důvodu zrušení**. | 
   | **Kód důvodu životní události** | Kód důvodu, který má být použit při výskytu životní události. |
   | **Kód důvodu změny sazby** | Kód důvodu, který má být použit při zrušení a opětovném otevření plánu zaměstnaneckých výhod během procesu aktualizace změny sazby. Informuje o tom, které záznamy byly změněny procesem aktualizace změny sazby. |
   | **Nově přijatý zaměstnanec je způsobilý** | Určuje, zda mají nově přijatí zaměstnanci nárok na podporu. |
   | **Období registrace nového zaměstnance** | Časové období, kdy je povolena registrace nově přijatého zaměstnance.</br></br>**Poznámka**: Toto nastavení přepíše jakékoli období registrace nově přijatého zaměstnance, které je nastaveno pro pravidlo nároku na plán. | 
   | **Životní události povoleny** | Povolí životní události. |
   | **Skrýt staré formuláře zaměstnaneckých výhod** | Umožňuje skrýt starší formuláře zaměstnaneckých výhod. |

3. Zvolte **Uložit**.

## <a name="configure-employee-self-service-parameters"></a>Konfigurace parametrů samoobsluhy zaměstnance

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry**.

2. Na kartě **Samoobsluha zaměstnance** zadejte hodnoty pro následující pole:

   | Pole | Popis |
   | --- | --- |
   | **Ověření zaměstnanecké výhody** | Ověřovací text, který se má použít při rezervaci výhod samoobsluhy. |
   | **Automatický výběr pověřených osob** | Určuje, zda mají být automaticky zvoleni následníci a příjemci na základě jejich nároku na možnosti plánu. |

3. Zvolte **Uložit**.
