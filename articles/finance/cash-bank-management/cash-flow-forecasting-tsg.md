---
title: Řešení potíží s nastavením předpovědi peněžních toků
description: Toto téma obsahuje odpovědi na otázky, které můžete mít při konfiguraci předpovědí peněžních toků. Řeší často kladené otázky (FAQ) týkající se nastavení peněžních toků, aktualizací peněžních toků a Power BI peněžních toků.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 39860a1960706aae7d223c8d2e810d39edc41b11deb80026925e6655f8e23ee8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747172"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Řešení potíží s nastavením předpovědi peněžních toků

[!include [banner](../includes/banner.md)]

Toto téma obsahuje odpovědi na otázky, které můžete mít při konfiguraci předpovědí peněžních toků. Řeší často kladené otázky (FAQ) týkající se nastavení peněžních toků, aktualizací peněžních toků a Power BI peněžních toků.

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>Proč se peněžní tok zobrazuje pouze u jedné právnické osoby?

Prognóza peněžních toků je konfigurována a vypočítávána podle právnické osoby. Zprávy Power BI a prognózy peněžních toků ve statistikách Finance Insights ukazují výsledky.

Pro každou právnickou osobu, pro kterou chcete zobrazit prognózu, je třeba nastavit prognózu peněžních toků. Zkontrolujte konfiguraci prognózy peněžních toků u všech vašich právnických osob. Alternativně zkontrolujte konfiguraci všech právnických osob na prognózu peněžních toků a ujistěte se, že jsou nastaveny tak, jak jste zamýšleli.

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>Proč Power BI nezobrazuje všechny údaje o peněžních tocích?

Než se mohou objevit prognózy peněžních toků v zobrazeních Power BI, je třeba provést několik kroků. Projděte si následující kontrolní seznam a ujistěte se, že byly provedeny všechny kroky:

- Nastavte peněžní tok pro každou právnickou osobu.
- V parametrech hlavní knihy nastavte systémovou měnu a typ směnného kurzu systému.
- Nastavte účetní měnu hlavní knihy a typ směnného kurzu.
- Zadejte směnný kurz mezi měnou transakce a zúčtovací měnou.
- Zadejte směnný kurz mezi zúčtovací měnou a měnou systému.
- Zadejte směnný kurz mezi zúčtovací měnou a měnami jednotlivých bank.

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>Proč peněžní tok Power BI fungoval v předchozích verzích, ale nyní je prázdný?

Ověřte, že byla nakonfigurována měření „Cash flow measure V2“ a „LedgerCovLiquidityMeasurement“ z úložiště Entity. Další informace o práci s daty v úložišti entit získáte v tématu [Integrace Power BI s úložištěm entit](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Ověřte, zda byly dokončeny všechny kroky potřebné k zobrazení obsahu Power BI. Další informace naleznete v tématu [Přehled hotovosti obsahu Power BI](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Byly entity úložiště Entity aktualizovány?

Musíte pravidelně obnovovat své entity, abyste zajistili, že data jsou aktuální a přesná. Chcete-li ručně aktualizovat konkrétní entitu, přejděte na **Správa systému \> Nastavení \> Úložiště Entity**, vyberte entitu a poté vyberte **Obnovit**. Data lze také aktualizovat automaticky. Na stránce **Úložiště Entity** nastavte možnost **Automatické obnovení povoleno** na **Ano**.

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a>Jakou metodu výpočtu je třeba použít při výpočtu prognóz cashflow?

Metoda výpočtu prognózy cashflow má dvě důležité možnosti výběru. Možnost **Nový** vypočítá prognózy cashflow pro nové dokumenty a dokumenty, které se změnily v době po spuštění poslední dávkové úlohy. Tato možnost obvykle probíhá rychleji, protože zpracovává menší podmnožinu dokumentů. Možnost **Celkem** přepočítá prognózy cashflow pro každý dokument v systému. Tato možnost trvá déle, protože má větší rozsah práce.

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a>Jak mohu zlepšit výkonnost opakující se dávkové úlohy předpovědi cashflow?

Doporučujeme předpovědi cashflow spouštět jednou za den mimo špičku a použít metodu výpočtu **Nový**. Doporučujeme používat tento přístup šest dní v týdnu. Poté jednou týdně spusťte prognózu cashflow využívající metodu výpočtu **Celkem**, a to v den s nejmenším množstvím aktivity.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

