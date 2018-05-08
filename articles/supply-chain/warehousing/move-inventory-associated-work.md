---
title: "Pohyb zásob s přidruženou prací v řízení skladu"
description: "Toto téma popisuje, jak nastavit a použít potvrzení výdeje kusů a registrační značky z mobilního zařízení."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7b330d6aa8e972d3c35bb7783ec0a39f09775011
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>Pohyb zásob s přidruženou prací v řízení skladu

[!include [banner](../includes/banner.md)]

Pomocí přesunu zásob, je možné rozhodnout, kteří pracovníci skladu mohou přesunout rezervované zásoby. Tím je zajištěna flexibilita v regulovaných skladech, kde se můžete rozhodnout nepovolil pracovníkovi zvolit nové místo vyskladnění pro již vytvořenou práci výdeje. Umožňuje také vedoucímu skladu řídit, které možnosti mají někteří méně zkušení pracovníci.

Flexibilita řízení každodenního provozu pracovníků skladu může být užitečné v situacích, jako jsou tyto:

## <a name="scenario-1"></a>Scénář 1
Společnost má poměrně malou oblast příjmu a je přetížena paletami a krabicemi, které čekají na vyskladnění. Očekává se velká dodávka v aktuální den, takže přijímající pracovník rozhodne uklidit oblast příjmu přesunutím některých palet do sekundární příchozí přípravné oblasti.

## <a name="scenario-2"></a>Scénář 2
Zkušený pracovník skladu zaznamená ve skladu příležitost konsolidovat položky v jenom místě, místo aby je bylo nutné rozdělit do tří nedalekých míst po malých množstvích. Pracovník chce sloučit množství přesunutím položek z každého takového skladového místa na stejné místo a se stejnou registrační značkou.

## <a name="scenario-3"></a>Scénář 3
Paleta čeká na dodávku do přechodného skladového místa, například STAGE01, který se nachází v BAYDOOR01. Z důvodu změny plánů však je však naplánován příjezd dodávky na BAYDOOR04. Úředník to ví a potřebuje mít jistotu, že dodávka nemusí čekat na naložení v místě STAGE01. Úředník rozhodne, že chcete převést položky v této dodávce z místa STAGE01 do STAGE04, které je blíž novému cíli.

### <a name="current-limitations"></a>Aktuální omezení

Rezervace práce, které lze přesunout, jsou omezeny na prodejní objednávku, převod objednávky výdeje, příjem objednávky převodu, nákupní objednávky a práci doplnění.

Přesunutí položek je omezeno, aby se zabránilo rozdělení řádků práce. To znamená, že pokud máte ze skladovacího místa Loc1 řádek práce pro 100 kusů položky A, nebude možné odtud přesunout pouze 30 kusů položky A do jiného umístění. Vzhledem k tomu, že skladová místa jsou nyní různá, znamenalo by to rozdělení řádku stávající práce na 30 a 70.

U scénářů fázování, kdy registrační značka, ze které přesouváte zboží, nebo registrační značka, na kterou přesouváte zboží, je nastavena jako cílová registrační značka pro výrobní příkaz platí, že je povolen pouze přesun celé registrační značky, aby se nerozdělila cílová registrační značka.
Pouze pohyb ad hoc je aktuálně podporován. To znamená, že nebudete moci přesunout rezervované zásoby prostřednictvím pohybu podle položek nabídky mobilního zařízení šablony.

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a>Nastavení oprávnění k přesunutí zásob rezervovaných pro jednotlivé pracovníky

U pracovníka, který má dovoleno přesunout rezervované zásoby, zaškrtněte políčko **Povolit pohyb zásob s přidruženou prací** ve skupinovém rámečku **řízení skladu** > **nastavení** > **pracovník**.  

### <a name="backported"></a>Přeneseno zpět

Tato funkce také byla přenesena zpět do aplikace Microsoft Dynamics AX 2012 R3 a bude dostupná v rámci CU12.
Lze ji stáhnout také samostatně prostřednictvím KB číslo 3192548. 


