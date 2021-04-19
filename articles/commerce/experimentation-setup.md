---
title: Nastavení experimentu
description: Toto téma popisuje, jak nastavit experiment ve službě třetí strany.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 9976ca461f7e988c32b81565fa2d084709e5ad6e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792500"
---
# <a name="set-up-an-experiment"></a>Nastavení experimentu

Jakmile [definujete hypotézu a určíte, jakou metriku úspěšnosti chcete používat](experimentation-identify.md), budete svůj experiment muset nastavit ve službě třetí strany. Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce. Další kroky jsou popsány v samostatných tématech.

[ ![Cesta uživatele experimentováním – nastavení](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Nastavení experimentu ve službě třetí strany
Nyní už byste měli mít vybranou službu třetí strany, abyste mohli spustit a monitorovat svůj experiment a nastavit konektor experimentování. Tyto předpoklady jsou uvedeny v tématu [Experimentování v Dynamics 365 Commerce](experimentation-overview.md).

Postupujte podle pokynů vyžadovaných k vytvoření experimentu ve službě třetí strany. Pokud je konektor správně nakonfigurován, objeví se kompletní seznam experimentů, které nastavíte ve službě třetí strany, v konfigurátoru webů Commerce asi do 5 minut.

## <a name="set-up-your-success-metrics"></a>Nastavení metriky úspěšnosti
Každý experiment potřebuje metriku k měření dopadu variant a k ověření hypotézy. Postupem podle pokynů níže povolte výpočet metriky ve službě třetí strany pomocí událostí živé telemetrie z Dynamics 365 Commerce.

Chcete-li nastavit metriku úspěšnosti, postupujte následujícím způsobem.

1. V konfigurátoru webů Commerce vyberte kartu **Stránky** v levém navigačním podokně a pak vyberte stránku, pro kterou chcete metriku shromažďovat. 
1. Přejděte do části **Sledovaná ID událostí** v pravém podokně vlastností stránky nebo modulu, který chcete sledovat.
1. Vyberte **Zobrazit**. Zobrazí se seznam všech ID událostí. Zkopírujte událost, kterou chcete sledovat, a vložte klíč této události do určeného umístění ve službě třetí strany. Pokud potřebujete více událostí, zkopírujte klíče postupně po jednom. 
    - Informace o tom, jak zobrazit všechny dostupné události a atributy včetně počtu zobrazení stránky a sledování tržeb, najdete v tématu [Události komponent Commerce pro diagnostiku a řešení potíží](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).
1. Proveďte všechny další kroky pro sledování metriky vyžadované službou třetí strany.

## <a name="previous-step"></a>Předchozí krok
[Identifikace hypotézy a určení metriky experimentu](experimentation-identify.md) 


## <a name="next-step"></a>Další krok
[Připojení a úpravy experimentu](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]