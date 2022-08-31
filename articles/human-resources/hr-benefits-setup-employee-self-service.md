---
title: Konfigurace samoobsluhy pro zaměstnance
description: V Microsoft Dynamics 365 Human Resources můžete konfigurovat dlaždice pro navigaci nejvyšší úrovní v samoobsluze pro zaměstnance.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cdc82c23635cc99c37aa770b996d9d2df43f5059
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324631"
---
# <a name="configure-employee-self-service"></a>Konfigurace samoobsluhy pro zaměstnance

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

V Microsoft Dynamics 365 Human Resources můžete konfigurovat dlaždice pro navigaci nejvyšší úrovní v **samoobsluze pro zaměstnance**. Dlaždice Plán zaměstnaneckých výhod směruje uživatele na plány zaměstnaneckých výhod, na něž mají nárok.

## <a name="set-up-a-benefit-plans-tile"></a>Nastavení dlaždice plánů zaměstnaneckých výhod

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry samoobsluhy zaměstnance**.

2. Vyberte kartu **Nastavení dlaždice plánu zaměstnaneckých výhod** a poté vyberte možnost **Nový**.

3. Zadejte hodnoty pro zbývající pole.

   | Pole | Popis |
   | --- | --- |
   | **Kód typu plánu** | Typ plánu, který se zobrazí, když je tato dlaždice vybrána v **samoobsluze zaměstnaneckých výhod**. |
   | **ID dlaždice** | Jedinečný identifikátor pro dlaždici. |
   | **Text popisku dlaždice** | Text, který se zobrazí v dlaždici **samoobsluhy zaměstnaneckých výhod**. |
   | **popis** | Popis dlaždice. |
   | **Obrázek pozadí dlaždice** | Adresa URL obrázku, který má být použit pro dlaždici (volitelné) |
   | **Sledování otevřené registrace** | Tuto možnost vyberte, chcete-li sledovat průběh otevřené registrace pro tento typ plánu. Například můžete mít vytvořené plány, kde **Typ plánu = Jiný**. Tyto plány mohou být volitelnými plány, u kterých nechcete sledovat průběh registrace. Pokud tento typ plánu nevyberete, na kartě **Otevřená registrace** bude ignorován při sledování průběhu registrace nebo při dokončení registrace. Toto nastavení platí pro typ plánu, který je vybrán pro všechna období a právnické osoby. |

4. Zvolte možnost **Uložit**.

## <a name="set-up-a-flex-credit-plan-tile"></a>Nastavení dlaždice plánu flexibilního kreditu

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry samoobsluhy zaměstnance**.

2. Vyberte kartu **Nastavení dlaždice plánu flexibilního kreditu** a poté vyberte možnost **Nový**.

3. Zadejte hodnoty pro zbývající pole.

   | Pole | Popis |
   | --- | --- |
   | **ID kreditu zaměstnaneckých výhod** | Plány programů flexibilních kreditů, které se zobrazí, když je tato dlaždice vybrána v **samoobsluze zaměstnaneckých výhod**. |
   | **ID dlaždice** | Jedinečný identifikátor pro dlaždici. |
   | **Text popisku dlaždice** | Text, který se zobrazí v dlaždici **samoobsluhy zaměstnaneckých výhod**. |
   | **popis** | Popis dlaždice. |
   | **Obrázek pozadí dlaždice** | Adresa URL obrázku, který má být použit pro dlaždici (volitelné) |
   | **Sledování otevřené registrace** | Tuto možnost vyberte, chcete-li sledovat průběh otevřené registrace pro tento typ plánu. Například můžete mít vytvořené plány, kde **Typ plánu = Jiný**. Tyto plány mohou být volitelnými plány, u kterých nechcete sledovat průběh registrace. Pokud tento typ plánu nevyberete, na kartě **Otevřená registrace** bude ignorován při sledování průběhu registrace nebo při dokončení registrace. Toto nastavení platí pro typ plánu, který je vybrán pro všechna období a právnické osoby. |

4. Zvolte možnost **Uložit**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
