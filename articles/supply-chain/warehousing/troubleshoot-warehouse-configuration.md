---
title: Odstraňování potíží s konfigurací skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při konfiguraci aplikace Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814385"
---
# <a name="troubleshoot-warehouse-configuration"></a>Odstraňování potíží s konfigurací skladu

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při konfiguraci aplikace Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Zobrazuje se následující chybová zpráva: „Registrační značka nebo skladové místo nejsou platné.“

### <a name="issue-description"></a>Popis problému

Tato chybová zpráva se zobrazí při skenování ID registrační značky nebo skladového místa.

### <a name="issue-resolution"></a>Řešení problému

Ujistěte se, že ID registrační značky není rezervováno něčím jiným. K tomuto problému docházelo, když hodnota, kterou uživatel naskenoval v mobilní aplikaci Řízení skladu, byla platným skladovým místem i platným ID registrační značky. Tento problém byl však vyřešen ve verzi 10.0.11.

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>Zobrazuje se následující chybová zpráva: „Pro toto skladové místo musí být určena registrační značka.“

### <a name="issue-description"></a>Popis problému

Tato chybová zpráva se zobrazí, pokud vytvoříte převodní příkaz pomocí skladu, který je povolen pro pokročilou správu skladu (WMS), a po dokončení práce se pokusíte potvrdit zásilku.

### <a name="issue-resolution"></a>Řešení problému

Pole **Výchozí skladové místo příjmu** je prázdné pro tranzitní sklad ze skladu. Chcete-li tento problém vyřešit, zadejte výchozí skladové místo příjmu v tranzitním skladu. Ujistěte se, že toto umístění je řízeno registrační značkou.

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>Zobrazuje se následující chybová zpráva: „Nelze vytvořit řádek pracovní šablony pro změnu stavu zásob, protože typ práce není platný. Vyberte jiný typ práce.“

### <a name="issue-description"></a>Popis problému

U pracovní šablony nemůžete vybrat *Změna stavu zásob* ve sloupci **Typ práce** sekce **Podrobnosti pracovní šablony**.

### <a name="issue-resolution"></a>Řešení problému

Toto chování je záměrné. Typ práce *Změna stavu zásob* používají pouze systémové procesy. Tento údaj nelze nakonfigurovat. Vzhledem k tomu, že seznam typů práce je opraven jako výčet, nelze nadbytečné položky odfiltrovat z rozevírací nabídky **Typ práce**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Zobrazuje se následující chybová zpráva: „Množství není platné pro jednotku 1%.“

### <a name="issue-description"></a>Popis problému

Množství není platné pro jednotku *ea* při práci výdeje, která má na jednom místě více registračních značek.

### <a name="issue-resolution"></a>Řešení problému

Ověřte, že pole **ID skupiny pořadí jednotek** a **Převody jednotek** na uvolněném produktu nebo variantě produktu jsou nastavena správně.

Upozorňujeme, že ve verzi 10.0.15 byla vylepšena chybová zpráva (viz [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Nová chybová zpráva zní: „Množství není platné. Očekáváno %1 %2."

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Ve směrnicích skladového místa pro práci vložení prodejní objednávky neuvádí možnost více SKU vyhodnocení více akcí směrnic skladového místa.

### <a name="issue-description"></a>Popis problému

Směrnice skladového místa typu pracovního příkazu *Prodejní objednávky* a typu práce *Vložení* nehodnotí více akcí směrnic skladového místa, když je vybrána možnost **Vícenásobné SKU**. Vyhodnocuje se pouze první akce směrnice skladového místa.

### <a name="issue-resolution"></a>Řešení problému

Ve verzi 10.0.15 byla přidána nová funkce *Vyhodnocení všech akcí pro směrnice skladového místa vícenásobného SKU* (viz [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Tato funkce vyhodnocuje všechny akce pro směrnice skladového místa vícenásobného SKU. Pokud požadujete tuto funkci, použijte [správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) k jejímu zapnutí.

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a>K částečnému výdeji nemohu použít mobilní aplikaci Řízení skladu.

### <a name="issue-description"></a>Popis problému

U prodejních objednávek a převodních příkazů nemůžete položky přeskočit a provést částečný výdej.

### <a name="issue-resolution"></a>Řešení problému

Na stránce **Položky nabídky mobilního zařízení** příkapro každou položku nabídky, která je nastavena na zpracování prodejních objednávek nebo převodních příkazů, nastavte možnost **Povolit rozdělení práce** na záložce s náhledem **Obecné** na *Ano*.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Jak mohu provést změnu stavu zásob u práce částečného množství?

### <a name="issue-description"></a>Popis problému

Chcete provést změnu stavu zásob u částečného množství dávky.

### <a name="issue-resolution"></a>Řešení problému

Chcete-li pracovníkům umožnit tuto změnu, můžete vytvořit položku nabídky pro mobilní aplikaci Řízení skladu. Na stránce **Položky nabídky mobilního zařízení** vytvořte (nebo upravte) položku nabídky, která má následující nastavení:

- **Režim:** *Práce*
- **Použít existující práci:** *Ne*
- **Proces tvorby práce:** *Pohyb*
- **Zobrazit stav zásob:** *Ano*

Na stránce můžete podle potřeby nastavit další pole.

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a>Profil správy dokování profilu umístění nebrání smíšení typů zásob.

### <a name="issue-description"></a>Popis problému

Používáte *zásady konsolidace dodávky*. Nastavili jste *profil správy doku* pro *profil umístění*, ale když je práce vytvořena, typy zásob se v konečném umístění smíchají.

### <a name="issue-resolution"></a>Řešení problému

Profily správy doků vyžadují, aby byla práce předem rozdělena. Jinými slovy, profil správy doku očekává, že pracovní záhlaví nebude mít více umístění pro vložení.

Aby profil správy doku mohl efektivně spravovat míchání zásob, musí být nastaveno zalomení pracovní hlavičky.

V tomto příkladu je náš profil správy doku nakonfigurován tak, že hodnota **Typy zásob, které by se neměly kombinovat** je nastavena na *ID zásilky* a nastavíme pro ni zalomení pracovní hlavičky:

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. Vyberte **Typ pracovního příkazu** pro úpravu (například *Nákupní objednávky*).
1. Vyberte pracovní šablonu, kterou chcete upravit.
1. V podokně akcí vyberte **Upravit dotaz**.
1. Otevřete kartu **Řazení** a přidejte řádek s následujícím nastavením:
    - **Tabulka** - *Dočasné pracovní transakce*
    - **Odvozená tabulka** - *Dočasné pracovní transakce*
    - **Pole** - *ID dodávky*
1. Vyberte **OK**.
1. Vrátíte se na stránku **Pracovní šablony**. V podokně akcí vyberte **Zalomení pracovních hlaviček**.
1. V podokně akcí vyberte **Upravit**.
1. Zaškrtněte políčko spojené s **Název pole** *ID zásilky*.
1. V podokně akcí vyberte **Uložit**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
