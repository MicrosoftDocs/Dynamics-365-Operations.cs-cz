---
title: Změna základu ve výpočtech daně ICMS-DIF pro produkty od dodavatelů z jiných států
description: Tento článek popisuje konfiguraci pro výpočty typu daně ICMS-DIF při obdržení fiskálního dokladu v brazilském státě Rio Grande do Sul (RS) nebo São Paulo (SP).
author: Kai-Cloud
ms.date: 06/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218642"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Změna základu (dvojitý základ) ve výpočtech daně ICMS-DIF pro produkty od dodavatelů z jiných států

Tento článek popisuje konfiguraci pro výpočty typu daně **ICMS-DIF** při obdržení fiskálního dokladu v brazilském státě Rio Grande do Sul (RS) nebo São Paulo (SP).

Podle definice ve státním zákoně se vybíraný Imposto sobre Circulação de Mercadorias e Serviços (ICMS) musí řídit tímto pravidlem:

*ICMS k výběru* = ([(*Operační částka* − *ICMS ze zdroje*) ÷ (1 − *ICMS % interní*)] × *ICMS % interní*) − *Částka ICMS ze zdroje*

## <a name="example"></a>Příklad

Brazilská společnost ve státě RS obdrží fiskální doklad o nákupu od prodejce ve státě SP. Společnost musí inkasovat procentuální rozdíl ICMS mezi státem RS (18 %) a státem SP (12 %). Základ však musí být vypočten podle předchozího pravidla.

- **Operační částka:** 1000,00 brazilských realů (1000,00 R$)
- **Mezistátní ICMS:** 120,00 R$
- **Procento ICMS ve státě RS:** 18 %
- **ICMS k výběr ve státě RS:** (\[(1000 − 120) ÷ (1 – 0,18)\] × 0,18) – 120 = 73,17 R$ 

## <a name="resolution"></a>Řešení

Chcete-li vypočítat rozdílové ICMS (ICMS-DIF) podle pravidel státu RS, musíte nastavit kódy daně z prodeje a skupinu daně z prodeje následujícím způsobem:

1. Vytvořte kód daně z prodeje pro příjem 12% ICMS (pro druhý stát). Tento kód se používá k registraci částky daňové pohledávky od dodavatele.
2. Vytvořte kód daně z prodeje pro výběr ICMS-DIF. Tento kód daně z prodeje by měl mít procentuální částku 18 % (pro váš vlastní stát), aby se definoval rozdíl mezi 18 % a 12 %. Nastavte typ daně na **ICMS-DIF**. Tento kód daně z prodeje musí být v parametrech výpočtu definován následujícím způsobem:

    - V poli **Původ** vyberte **Procento hrubé částky**.
    - V poli **Základ marže** vyberte **Čistá částka na řádek**.
    - Definujte daňový kód tak, aby měl fiskální hodnotu **3**. Tímto způsobem bude opravná transakce automaticky vytvořena, když je aktivní modul **Fiskální knihy**.
    - V konfiguraci skupiny daně z prodeje vyberte možnost **Použít daň** pro kód daně z prodeje **ICMS-DIF**.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>Použití rozdílové daňové sazby v konfiguraci kódů DPH ICMS-DIF s dvojím základem

Při použití výše popsaných nastavení kód DPH **ICMS-DIF** bude vypočítán podle pravidla dvojího základu. Nominální daňová sazba však bude 18 procent, což se od 6procentní sazby liší jednoduchým základním pravidlem. Tento rozdíl způsobuje problémy s nekonzistencí ve fiskálních dokladech a daňovém hlášení. Od Microsoft Dynamics 365 Finance verze 10.0.29 můžete aktivovat funkci **(Brazílie) Nakonfigurovat rozdílovou daňovou sazbu v daňovém kódu ICMS-DIF pro případy dvojího základu** ve **Správě funkcí** k odstranění nesrovnalosti.

- Kromě provedení kroků v předchozí části vyberte kód DPH **ICMS 12** v poli **DPH na DPH**.
- Nastavte sazbu daně kódu DPH **ICMS-DIF** na 18 procent. Pole **Procento/částka** zobrazí nominální daňovou sazbu jako 6 procent.

> [!NOTE]
> Kódy DPH **ICMS-DIF** a **ICMS 12** musí být přiřazeny ve stejné skupině DPH.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>Změna základu (dvojitý základ) ve výpočtech daně ICMS-DIF pro produkty pro zákazníky neplátce daně (DIFAL) z jiných států

Aktivujte funkci **(Brazílie) Výpočet dvojího základu pro ICMS-DIFAL v prodejních transakcích** ve **Správě funkcí** na podporu změny základu ICMS-DIF při obchodování se zákazníky z jiného státu, kteří nejsou plátci daně. Ukázkový kód DPH ICMS-DIF vstoupí v platnost v transakcích prodejní objednávky a faktury s volným textem.

Aktivujte funkci **(Brazílie) Výpočet dvojího základu pro ICMS-DIFAL pro případy IPI** ve **Správě funkcí** na podporu scénářů obchodování se zákazníky, kteří nejsou plátci daně z jiného státu, které je rovněž povinné k Imposto sobre Produtos Industrializados (IPI). Částka daně z kódu DPH IPI bude uznána a uplatněna v základu daně ICMS-DIFAL.

- V záhlaví prodejní objednávky nebo faktury s volným textem na pevné záložce **Fiskální údaje** musí být možnost **Koncový uživatel** nastavena na **Ano**.
- V záhlaví nákupní objednávky nebo faktury dodavatele na pevné záložce **Fiskální údaje** musí být možnost **Použití a spotřeba** nastavena na **Ano**.
