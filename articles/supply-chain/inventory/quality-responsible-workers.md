---
title: Zaměstnanci odpovědní za schvalování neshod
description: Toto téma popisuje, jak konfigurovat pracovníky odpovědné za schvalování neshod.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fd1c7c86ac8627bd332bc578e98b4d7f091cdc8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575889"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>Zaměstnanci odpovědní za schvalování neshod

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak konfigurovat pracovníky odpovědné za schvalování neshod.

Neshody musí být schváleny, než uživatelé mohou začít zadávat podrobnosti, jako jsou opravy nebo operace. Než uživatelé mohou schválit nebo odmítnout neshody, musí být jejich ID uživatele (záznam uživatele) propojeno se záznamem pracovníka. Můžete volitelně nakonfigurovat pracovníky, kteří jsou zodpovědní za kvalitu, a poté jednomu pracovníkovi povolit schválení práce jménem jiného pracovníka.

## <a name="enable-a-user-for-nonconformance-processing"></a>Povolení zpracování neshody uživateli

Než uživatel může schválit nebo odmítnout neshody, musíte jeho záznam uživatele propojit se záznamem pracovníka. Pole schválení lze poté nastavit automaticky a aktuálního uživatele lze automaticky vyplnit pro časový rozvrh. Než může uživatel použít poznámky k dokumentům, musíte v jeho v možnostech uživatele aktivovat manipulaci s dokumenty.

1. Přejděte do nabídky **Správa systému \> Uživatelé \> Uživatelé**.
1. Najděte a otevřete uživatele, který by měl být schopen schválit nebo odmítnout neshody.
1. Nastavte pole **Osoba** na jméno pracovníka, který souvisí s aktuálním záznamem uživatele.
1. V podokně akcí vyberte volbu **Možnosti uživatele**.
1. Na stránce **Možnosti** pro aktuální záznam uživatele nastavte na kartě **Předvolby** možnost **Povolit manipulaci s dokumenty** na hodnotu *Ano*.
1. Zavřete stránky.

## <a name="define-workers-that-are-responsible-for-quality"></a>Definování pracovníků odpovědných za kvalitu

1. Přejděte k nabídce **Řízení zásob \> Nastavení \> Řízení kvality \> Pracovníci odpovědní za kvalitu**.
2. V podokně akcí zvolte **Nový**.
3. V poli **Pracovník** vyberte pracovníka, který zadává data o kvalitě.
4. V poli **Odpovědný pracovník** vyberte pracovníka, pro kterého vybraný pracovník zadává práci jeho jménem. Když se vytvoří a aktualizují neshody, bude tento pracovník ve výchozím nastavení zadán v polích **Pracovník**.

## <a name="additional-resources"></a>Další prostředky

- [Přehled správy kvality](quality-management-processes.md)
- [Povolit správu kvality a neshod](enable-quality-management.md)
- [Náklady kvality](quality-charges.md)
- [Karanténní zóny pro neshody](quality-quarantine-zones.md)
- [Diagnostické typy pro neshody](quality-diagnostic-types.md)
- [Kódy kvality pro náklady.](quality-charges.md)
- [Operace pro neshody](quality-operations.md)
- [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
