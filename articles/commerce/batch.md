---
title: Vylepšené zpracování položek sledovaných dávkou
description: Toto téma popisuje vylepšené zpracování položek sledovaných dávkou během procesu zaúčtování příkazu. Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/09/2021
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
ms.openlocfilehash: 513b6ca84fa71e851a5a3e4275e0b6572789e1eb
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485776"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Vylepšené zpracování položek sledovaných dávkou

[!include [banner](includes/banner.md)]

Toto téma popisuje vylepšené zpracování položek sledovaných dávkou během procesu zaúčtování příkazu. Microsoft Dynamics 365 Commerce.

Na Dynamics 365 Commerce pokladním místě (POS) nelze zaznamenat čísla dávek pro položky sledované dávkou v okamžiku prodeje. Nicméně pro konkrétní konfigurace při zaúčtování prodejů v Commerce Headquarters prostřednictvím objednávek zákazníků nebo zaúčtování příkazů očekává aplikace Commerce, že platná čísla dávky pro položky sledované dávkou existují, a že budou použity během procesu fakturace.

Pokud jsou pro produkty k dispozici platná čísla dávek, použije je proces fakturace objednávky zákazníka i proces fakturace prodejní objednávky ze zaúčtování příkazu. Pokud pro produkty nejsou k dispozici platná čísla dávek, proces fakturace objednávky zákazníka nemůže zaúčtovat a uživatel POS obdrží chybovou zprávu. Účtování příkazů pak přejde do chybového stavu, i když byly u produktů zapnuty negativní zásoby.

Vylepšení, která byla provedena v aplikaci Commerce pomáhají zajistit, že při zapnutých záporných zásobách pro položky sledované dávkou nebudou pro tyto položky blokovány fakturace objednávek zákazníků a fakturace prodejních objednávek prostřednictvím zaúčtování příkazu, pokud jsou zásoby 0 (nula) nebo není k dispozici číslo dávky. Nová vylepšená funkcionalita používá výchozí ID dávky pro prodejní řádky, když nejsou čísla dávek k dispozici.

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>Definujte výchozí ID dávky, které se používá pro objednávky zákazníků

Postup definování výchozího ID dávky, které se používá pro objednávky zákazníků:

1. V aplikaci Commerce Headquarters přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry aplikace Commerce**.
1. Na kartě **Objednávky zákazníků**, na záložce s náhledem **Objednat** zadejte hodnotu do pole **Výchozí ID dávky**.

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>Definujte výchozí ID dávky, které se používá pro fakturaci prodejní objednávky prostřednictvím zaúčtování příkazu

Postup definování výchozí ID dávky, které se používá pro fakturaci prodejní objednávky prostřednictvím zaúčtování příkazu:

1. V aplikaci Commerce Headquarters přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry aplikace Commerce**.
1. Na kartě **Zaúčtování**, na záložce s náhledem **Aktualizace zásob** zadejte hodnotu do pole **Výchozí ID dávky**.

> [!NOTE]
> - Funkce výchozí ID dávky je k dispozici pouze tehdy, když je povolena rozšířená správa skladu pro konkrétní sklad obchodu a položky. V další vydané verzi bude tato funkcionalita výchozí ID dávky podporována též pro scénáře, kde rozšířená správa skladu není povolena.
> - Podpora pro zlepšené zpracování položek sledovaných dávkou při zaúčtování příkazu pro nerozšířené scénáře správy skladu byla představena ve vydané verzi aplikace Commerce verze 10.0.5.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
