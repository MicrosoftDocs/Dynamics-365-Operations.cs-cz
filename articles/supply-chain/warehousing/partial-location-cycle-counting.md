---
title: Částečná cyklická inventura místa
description: Aktuální operace výpočtů řídí plány cyklické inventury. Můžete požadovat, aby byly započítány pouze konkrétní produkty a varianty produktů namísto všech zásob na skladě ve skladovém místě.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f07c7754dbe36334e8972d49edf9fb84a78f5d0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215670"
---
# <a name="partial-location-cycle-counting"></a>Částečná cyklická inventura místa

[!include [banner](../includes/banner.md)]

Aktuální operace výpočtů řídí plány cyklické inventury. Můžete požadovat, aby byly započítány pouze konkrétní produkty a varianty produktů namísto všech zásob na skladě ve skladovém místě.

Když použijete plány cyklické inventury k vytvoření prací na inventuře, můžete řídit vlastní inventurní operace. Můžete požadovat, aby byly započítány pouze konkrétní produkty a varianty produktů namísto všech zásob na skladě ve skladovém místě. Vyfiltrováním konkrétních produktů může vedoucí skladu snížit kontrolu režie, vyhnout se chybám konsolidace a ušetřit čas.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Konfigurace cyklické inventury částečného místa
Když použijete proces práce ve skladu pro skladové operace inventury, pro každé místo se vytvoří záhlaví práce. Při definování plánu cyklické inventury můžete použít dotaz **Vybrat umístění** k omezení vytvořené práce cyklické inventury. Vyberete-li produkty pro plán cyklické inventury, můžete vybrat dotazy na produkt a variantu produktu k upřesnění toho, co je do inventury zahrnuto. 

Můžete přidružit **šablonu práce** k plánu cyklické inventury pro definování, jak by měla být vytvořena práce cyklické inventury. Šablona práce pro operace inventury přímo odkazuje na plán cyklické inventury. 

Při definování podrobností šablony práce můžete vybrat možnost **Zalomení řádků práce** k určení, zda řádky práce na inventuře musí být seskupeny podle čísla položky nebo varianty produktu. Toto nastavení není povinné, pokud chcete provést výpočet zásob na skladě pouze pro konkrétní produkty ve skladovém místě. Řádky práce cyklické inventury, které jsou vytvořeny, budou mít úroveň informací, kterou zde definujete, a řízené cyklické operace budou zpracovány na základě této úrovně. 

Pokud přiřadíte plány cyklické inventury šablonám práce pomocí možnosti **Zalomení řádků práce**, je vybráno pole **částečné cyklické inventury** pro vybranou práci cyklické inventury, která je vytvořena, a vytvoří se více řádků práce cyklické inventury na základě definice pracovní šablony. 

Předtím, než lze zpracovat práci cyklické inventury, musíte přinejmenším zaškrtnout políčko **Zobrazit číslo položky** nabídky mobilního zařízení v rámci nastavení cyklické inventury. Operátor skladu bude požádán o zaznamenání pouze těch informací o inventuře, které souvisí s řádky inventury (čísla položky a dimenze produktů). Všechny ostatní zásoby na skladě budou v tomto procesu inventury ignorovány. 

Pro proces částečné cyklické inventury nebude datum/čas **poslední cyklické inventury** pro skladové místo aktualizovány.

## <a name="example"></a>Příklad
V tomto příkladu se pro sklad 61 musí započítat pouze číslo položky A0001.

1.  Je vytvořena nová šablona práce pro cyklickou inventuru. Možnost **Zalomení řádků práce** se používá k seskupení řádek práce inventury podle čísla položky. Proto bude vytvořená práce výpočtu cyklické inventury mít řádky na číslo položky. Také můžete seskupit řádky podle čísla varianty produktu.
2.  Je vytvořen nový plán cyklické inventury, který odkazuje na nově vytvořenou šablonu práce. Plán cyklické inventury zahrnuje všechna místa ve skladu 61 (dotaz **vybrat umístění**), které blokuje zásoby s číslem položky A0001. Výběr konkrétních produktů je definován v oddílu **Výběr produktů cyklické inventury**.
3.  Můžete vybrat produkty pro plány cyklické inventury pomocí nastavení pole **Prázdná skladová místa** na **Vyloučit prázdná**. Při zpracování plánu cyklické inventury je vytvořena práce částečné cyklické inventury pro číslo položky A0001. Skutečný proces inventury lze provést pomocí položky nabídky mobilního zařízení pro řízené cyklické inventury.



<a name="additional-resources"></a>Další zdroje
--------

[Cyklická inventura](cycle-counting.md)

