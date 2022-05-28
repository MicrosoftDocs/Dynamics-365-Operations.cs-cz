---
title: Předpovědi plateb zákazníka
description: Toto téma popisuje předpovědi plateb, která mohou pomoci lépe porozumět typickým platebním praktikám zákazníků. Tato funkce vám také mpže pomoci identifikovat okolnosti, kdy byste měli zahájit proces inkasa dříve, než byste to zahájili v ostatních případech.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f3d6f328ff3fd4da6ad3e7d4f3f751d3be692736
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713183"
---
# <a name="customer-payment-predictions"></a>Předpovědi plateb zákazníka

[!include [banner](../includes/banner.md)]

Toto téma popisuje předpovědi plateb, která mohou pomoci lépe porozumět typickým platebním praktikám zákazníků. Tato funkce vám také může pomoci identifikovat okolnosti, kdy byste měli zahájit proces inkas dříve, než byste to zahájili v ostatních případech.

## <a name="overview"></a>Přehled

Organizace často považují za náročné předvídat, kdy zákazník zaplatí faktury. Tento nedostatek informací může způsobit následující problémy:

- Méně přesné předpovědi peněžních toků
- Procesy inkasa, které začínají příliš pozdě
- Objednávky, které jsou vydávány zákazníkům, u nichž může dojít k selhání platby

Předpovědi plateb zákazníka pomáhá organizacím předpovědět, kdy dojde k zaplacení faktury zákazníkem. Proto mohou vytvářet strategie sbírek, které pomáhají zvyšovat pravděpodobnost, že budou zaplaceny včas.

## <a name="predictions"></a>Předpovědi

Předpovědi plateb umožňují organizacím vylepšit jejich obchodní procesy tím, že jim pomohou identifikovat faktury, u nichž je pravděpodobné, že budou zaplaceny pozdě. Organizace může tyto informace použít k provedení akcí, které zvýší pravděpodobnost, že budou zaplaceny včas.

Funkce předpovědi plateb zákazníka používá model strojového učení k přesnějším předpovědím, kdy zákazník zaplatí neuhrazenou fakturu. Tento model strojového učení zahrnuje historické faktury, platby a údaje o zákaznících.

Pro každou otevřenou fakturu funkce přiřadí tři pravděpodobnosti platby:

- Pravděpodobnost, že bude platba provedena včas
- Pravděpodobnost, že bude platba provedena pozdě
- Pravděpodobnost, že bude platba provedena velmi pozdě

Tato funkce také poskytuje souhrnný pohled na očekávané platby.

[![Agregované zobrazení předpovědí platby.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Každá faktura má přiřazenou pravděpodobnost platby včas. Faktury, jejichž pravděpodobnost včasné úhrady je nižší než 50 %, budou označeny červeným kroužkem, což znamená, že mohou vyžadovat pozornost inkasního agenta.

[![Seznam pravděpodobností platby.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Funkce Zákaznické předpovědi plateb také poskytuje kontextové informace vysvětlující předpovědi. Tyto informace zahrnují hlavní faktory, které ovlivnily predikci, aktuální stav obchodu se zákazníkem a podrobnosti o historickém platebním chování zákazníka.

V mnoha podnicích je proces inkasa reaktivní činností. Jinými slovy, proces inkasa se nespustí, dokud nebudou faktury splatné. Aplikace Přehledy plateb zákazníka (Preview) umožňuje organizacím být aktivnější v oblasti inkas. Již nemusí čekat na to, až bude transakce splatná, aby mohl být zahájen proces inkasa. Namísto toho mohou pomocí možnosti předpovědí plateb určit, zda provedená aktivní inkasa zvýší pravděpodobnost včasných plateb.

## <a name="methodology"></a>Metodologie

V minulosti bylo obvykle obtížné vyvinout a nasadit řešení umělé inteligence (AI). Proces vyžaduje tým, který obsahuje datové vědce, odborníky na dané záležitosti a techniky, kteří pracují dlouhou dobu na formulování, vývoji, nasazení a udržování použitelného řešení AI. Předpovědi plateb zákazníků usnadňují nasazení a používání řešení umělé inteligence v Microsoft Dynamics 365 Finance. Společnost Microsoft dodává řešení AI vybudovaná na aplikaci Microsoft AI Builder. Uživatelé proto mohou nasadit řešení AI jediným kliknutím myši a využít výhod inteligentních předpovědí. Pokud nejste spokojeni s přesností předpovědi, může uživatel power user (znovu jedním kliknutím myši) spustit prostředí rozšíření aplikace AI Builder a poté vybrat nebo zrušit výběr polí používaných k vygenerování předpovědi. Až budete připraveni, můžete model „vytrénovat“ a publikovat změny. Nově trénovaný model se automaticky spustí a vygeneruje předpovědi v Dynamics 365 Finance.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
