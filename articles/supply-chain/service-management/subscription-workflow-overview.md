---
title: "Přehled workflowu odběru"
description: "Toto téma poskytuje přehled workflowu předplatného."
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b4872c0753b54bdddf2c7778a13819726eea4a90
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---


# <a name="subscription-workflow-overview"></a>Přehled workflowu odběru 

[!include [banner](../includes/banner.md)]


Pracujete jako správce předplatného pro společnost pronajímající osvětlovací techniku a že vaše společnost nabízí předplatné pro údržbu osvětlovacích techniky. Zákazník kontaktuje vaši společnost s cílem zakoupit roční předplatné zahrnující údržbu systému osvětlení.

## <a name="setting-up-subscriptions"></a>Nastavení předplatného

Při nastavení předplatného musíte nejprve vytvořit skupinu předplatného pro novou servisní smlouvu nebo ověření existence skupiny předplatného. Pokud skupina ověření předplatného existuje, musí pro ni být nastavena frekvence ročního fakturování odběratele a musí umožňovat časové rozlišení prodejního zisku pro každý měsíc v roce. Další informace o postupu při nastavení předplatných získáte v tématu [Nastavení skupin předplatného](set-up-subscription-groups.md).

Po vytvoření skupiny předplatného můžete vytvořit předplatné. Další informace o vytvoření předplatného servisu naleznete v tématu [Vytvoření předplatného servisu ze skupiny předplatného ](create-service-subscriptions-from-subscription-group.md).

## <a name="create-and-modify-subscription-transactions"></a>Vytvoření a úprava transakcí předplatného

Po nastavení předplatného vytvoříte transakci poplatku předplatného pro první fakturační období, což je jeden rok. Transakce jsou typu **Běžné**. To znamená, že lze vytvořit pouze transakce předplatného, u nichž hodnoty Od data a Do data odpovídají existujícím obdobím vytvořeným ve formuláři **Typy období**. Další informace o transakcích poplatků naleznete v tématu [Vytvoření transakcí poplatků předplatného](create-subscription-fee-transactions.md).

Po nastavení předplatného pro určitého odběratele si vzpomenete, že tento odběratel si s vámi dojednal slevu ve výši 10 procent na všechny ceny z ceníku nabízených služeb. Z tohoto důvodu budete muset snížit vytvořenou cenu poplatku transakce.

Později ve stejný den se s vámi telefonicky spojí kontaktní osoba zákazníka a sdělí vám, že nadále požadují servisní smlouvu pro systém osvětlení, avšak že později v průběhu roku plánují instalaci nového systému osvětlení. Z tohoto důvodu je požadován rozsah smlouvy jen do října 2013. S cílem snížení počtu měsíců pro předplatné zákazníka vytvoříte novou transakci poplatku předplatného typu **Dny omezení**. Další informace o tom, jak snížit počet dní, lze najít v tématu [snížení počtu dnů u poplatků za odběr](reduce-the-days-on-subscription-fees.md).

## <a name="invoice-and-accrue-subscription-transactions"></a>Fakturace a časové rozlišení pro transakce předplatného

Nyní jste dokončili nastavení předplatného a jste připraveni na fakturaci předplatného pro odběratele. Další informace o postupu při fakturaci předplatných získáte v tématu [Fakturace skupin předplatného](invoice-subscription-transactions.md).

O dva dny později se s vámi odběratel spojí telefonicky a požaduje, aby předplatné bylo fakturováno v amerických dolarech, a nikoli v eurech. Proto vytvoříte dobropis a poté vytvoříte novou transakci předplatného ve správné měně. Další informace o postupu při úvěrování předplatných transakcí získáte v tématu [Fakturace skupin předplatného](credit-subscription-transactions.md).

Na konci každého měsíce připíšete časově rozlišené výnosy z předplatného odběratele na účet zisků a ztrát a na účty WIP. Další informace o postupu při časovém rozlišení pro předplatné získáte v části [časově rozlišené výnosy předplatného](accrue-subscription-revenue.md).

  



