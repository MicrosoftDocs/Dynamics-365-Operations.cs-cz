---
title: Vylepšené zpracování položek sledovaných dávkou
description: Toto téma popisuje vylepšení provedená u zpracování dávek pro položky sledované dávkou během procesu zaúčtování výkazu.
author: josaw1
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2453ed711d47e062c82d3888ff471b770b5bb2ef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799702"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Vylepšené zpracování položek sledovaných dávkou


[!include [banner](includes/banner.md)]


V Point of Sale (POS) nelze zaznamenat čísla dávek pro položky sledované dávkou v okamžiku prodeje. Nicméně pro konkrétní konfigurace při zaúčtování prodejů v centrále prostřednictvím objednávek zákazníků nebo zaúčtování výkazů očekává systém Microsoft Dynamics, že platná čísla dávky pro položky sledované dávkou existují a že budou použity během procesu fakturace.

Pokud jsou pro produkty k dispozici platná čísla dávek, použije je proces fakturace objednávky zákazníka a proces fakturace prodejní objednávky ze zaúčtování výkazu. V opačném případě proces fakturace objednávky zákazníka nemůže provést zaúčtování a uživatel POS obdrží chybovou zprávu. Zaúčtování výkazu se pak dostane do chybového stavu. K tomuto chybovému stavu dojde tehdy, když byly pro produkty zapnuty záporné zásoby.

Vylepšení, která byla provedena v aplikaci Retail verze 10.0.4 a novějších, pomáhají zaručit, že při zapnutých záporných zásobách pro položky sledované dávkou nebudou pro tyto položky blokovány fakturace objednávek zákazníků a fakturace prodejních objednávek prostřednictvím zaúčtování výkazu, pokud jsou zásoby 0 (nula) nebo není k dispozici číslo dávky. Nová funkcionalita používá výchozí ID dávky pro prodejní řádky, když nejsou čísla dávek k dispozici.

Chcete-li definovat výchozí ID dávky, které se používá pro objednávky zákazníka, na stránce **Parametry obchodu** na kartě **Objednávky zákazníka** na záložce s náhledem **Objednávka** nastavte pole **Výchozí ID dávky**.

Chcete-li definovat výchozí ID dávky, které se používá pro fakturaci prodejní objednávky prostřednictvím zaúčtování výkazu, na stránce **Parametry obchodu** na kartě **Zaúčtování** na záložce s náhledem **Aktualizace zásob** nastavte pole **Výchozí ID dávky**.

> [!NOTE]
> Tato funkce je k dispozici pouze tehdy, když je zapnuta rozšířená správa skladu pro konkrétní sklad obchodu a položky. V novější verzi bude tato funkcionalita podporována též pro scénáře, kde se rozšířená správa skladu nepoužívá.

> [!NOTE]
> Podpora pro zlepšené zpracování položek sledovaných dávkou při zaúčtování výkazů pro nerozšířené scénáře správy skladu byla představena v aplikaci Retail verze 10.0.5.


[!INCLUDE[footer-include](../includes/footer-banner.md)]