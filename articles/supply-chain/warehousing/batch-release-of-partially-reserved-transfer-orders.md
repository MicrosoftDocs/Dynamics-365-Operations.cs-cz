---
title: Vydání dávky částečně rezervovaných převodních příkazů
description: Tento článek popisuje, jak nastavit a použít vydání dávky částečně rezervovaných převodních příkazů z mobilního zařízení.
author: perlynne
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0b21c0000f6bf1cbbb318c898a519e51ca7e9b8
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068624"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Vydání dávky částečně rezervovaných převodních příkazů

[!include [banner](../includes/banner.md)]

Funkce pro vydání dávky částečně rezervovaných převodních příkazů umožňuje částečně vydat převodní příkazy do skladu pomocí dávkové úlohy.
Vzhledem k tomu, že máte možnost vydat částečné množství, nemusíte čekat, než bude celé množství objednávky k dispozici ve skladu předtím, než objednávku vydáte.

Vydání objednávek pro sklad je proces správy skladu (WMS). Tento proces zahrnuje činnosti jako například výdej, balení a expedici, které může pracovník skladu provést pomocí mobilního zařízení.

## <a name="where-it-applies"></a>Kdy se to používá

Pro tuto funkci jsou převodní příkazy vydány do skladu pomocí dávkové úlohy. Tato funkce je užitečná, pokud nemáte dostatek zásob ve skladu, ale stále chcete převést zboží z jednoho skladu do druhého.

## <a name="how-it-is-set-up"></a>Způsob nastavení

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Určení kritérií plnění pro převodní příkazy a prodejní objednávky

Než může být objednávka částečně uvolněna do skladu v dávce, musí být splněna kritéria plnění. Tato kritéria plnění jsou určena zásadami plnění.

Zásady plnění pro převodní příkazy a prodejní objednávky jsou určené na úrovni společnosti. V závislosti na nastavení zásad plnění bude vydání objednávek v dávce přijato nebo zamítnuto. Objednávky budou poté podle toho zpracovány.

-   Chcete-li vytvořit zásady plnění pro převodní příkazy a prodejní objednávky, klikněte na **Řízení skladu** \> **Nastavení** \> **Uvolnit do skladu** \> **Zásady plnění** a pak vytvořte zásadu plnění zadáním názvu a popisu.

-   Chcete-li určit sazbu plnění, typ hodnoty a zprávu, která se zobrazí v případě porušení zásady plnění, klikněte na **Řízení skladu** \> **Nastavení** \> **Uvolnit do skladu** \> **Zásady plnění** a následně nastavte pole **Sazba plnění**, **Typ hodnoty** a **Zprávy porušení plnění**.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Nastavení zásad plnění pro převodní příkazy a prodejní objednávky

-   Chcete-li nastavit zásady plnění pro převodní příkazy, klikněte **Řízení zásob** \> **Nastavení** \> **Parametry modulu Řízení zásob a skladu** \> **Převodní příkazy** \> **Řízení skladu** a poté vyberte zásadu plnění převodních příkazů.

-   Chcete-li nastavit zásady plnění pro prodejní objednávky, klikněte na **Pohledávky** \> **Nastavení** \> **Parametry pohledávek** \> **Řízení skladu** a poté vyberte zásadu plnění prodejní objednávky.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a>Povolení vydání v dávce a určení množství, které je třeba uvolnit v dávce

Dávková úloha se používá k uvolnění objednávek do skladu v dávce. Parametry rozlišující objednávky, které mají být spuštěny v dávkové úloze, se nastavují na samotné dávkové úloze.

Parametr **Množství** určuje, zda má být v dávce uvolněné fyzicky rezervované množství nebo celé množství. Parametr **Povolit uvolnění částečně uvolněných objednávek** určuje, zda by objednávky v dávce měly být přijaty nebo zamítnuty, pokud byly částečně uvolněny dříve.

-   Chcete-li nastavit **množství** a **Povolit uvolnění částečně uvolněných objednávek** pro převodní příkazy, klikněte na **Řízení skladu** \> **Uvolnit do skladu** \> **Automaticky uvolnit převodní příkazy**.

-   Chcete-li nastavit **množství** a **Povolit uvolnění částečně uvolněných objednávek** pro prodejní objednávky, klikněte na **Řízení skladu** \> **Uvolnit do skladu** \> **Automaticky uvolnit prodejní objednávky**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]