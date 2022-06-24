---
title: Nastavení účtů pro zaúčtování leasingu
description: Tento článek uvádí seznam účtů pro zaúčtování, které jsou vyžadovány pro transakce leasingu majetku, a vysvětluje, jak definovat účty pro zaúčtování na stránce Parametry účtování leasingu.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6e3a0d8dd3bb3e58ca10b2efce0cc88a2f48d2de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859907"
---
# <a name="set-up-lease-posting-accounts"></a>Nastavení účtů pro zaúčtování leasingu

[!include [banner](../includes/banner.md)]

Tento článek uvádí seznam účtů pro zaúčtování, které jsou vyžadovány pro transakce leasingu majetku, a vysvětluje, jak definovat účty pro zaúčtování na stránce **Parametry účtování leasingu**.

Abyste vyhověli tématu Kodifikace účetních standardů 842 (ASC 842) a Mezinárodnímu standardu účetního výkaznictví 16 (IFRS 16), možná budete muset vytvořit účty ve svém účtovém rozvrhu. Účty, které vytvoříte, aby vyhovovaly standardům ASC a IFRS, však nejsou účty dlouhodobých aktiv. Podle ASC 842 se aktivum s právem na užívání (ROU) zaznamenává jak u finančního, tak u operativního leasingu. Tyto leasingy jsou oddělené od stálých aktiv. (Používaný majetek můžete stále udržovat pomocí dlouhodobého majetku.)

Další informace, jak vytvořit účetní struktury, najdete v části [Vytvoření účetních struktur](../general-ledger/tasks/create-account-structures.md). Další informace, jak vytvořit hlavní účet, najdete v části [Vytvoření hlavního účtu](../general-ledger/tasks/create-main-account.md).

V následující tabulce jsou uvedeny příklady účtů, které musíte vytvořit pro transakce pronajatých aktiv, pokud ještě nebyly vytvořeny. Podle IFRS 16 se vztahy operativního leasingu stále používají pro krátkodobé a krátkodobé leasingy.

| Číslo účtu hlavní knihy | Typ účtu  | Název účtu                                          |
|-----------------------|---------------|-------------------------------------------------------|
| 180150                | Materiál         | Aktivita používaného majetku                                     |
| 180160                | Materiál         | Budování používaného majetku                                    |
| 180250                | Materiál         | Kredit: Akumulovaný odpis XXX – vozidla                   |
| 180260                | Materiál         | Kredit: Akumulovaný odpis – budovy                  |
| 222300                | Pasiva     | Krátkodobý závazek – finanční leasing                |
| 222310                | Rozvaha | Krátkodobý závazek – operativní leasing              |
| 250200                | Pasiva     | Úpisy – závazky                                         |
| 250601                | Rozvaha | Dlouhodobý závazek – finanční leasing                 |
| 250602                | Rozvaha | Dlouhodobý závazek – operativní leasing               |
| 250606                | Rozvaha | Odložená splátka                                         |
| 300160                | Rozvaha | Pozdržené příjmy                                     |
| 604500                | Expense       | Výdaje na leasing                                         |
| 604501                | Expense       | Náklady na operativní leasing vozidla – nárůst úroků  |
| 604502                | Expense       | Náklady na operativní leasing vozidla – amortizace        |
| 605200                | Expense       | Náklady na operativní leasing budovy – nárůst úroků |
| 605201                | Expense       | Náklady na operativní leasing budovy – amortizace       |
| 607101                | Expense       | Náklady na leasing vozidla                    |
| 607102                | Expense       | Náklady na leasing budovy                   |
| 607103                | Expense       | Snížení hodnoty - finanční leasing                   |
| 607104                | Expense       | Snížení hodnoty - operativní leasing                 |
| 618910                | Expense       | Náklady na leasing - finanční leasing                        |
| 618920                | Expense       | Variabilní platby - finanční leasing                    |
| 618930                | Expense       | Variabilní platby - operativní leasing                  |
| 800600                | Expense       | Úrokové náklady na leasing vozidla                        |
| 800601                | Expense       | Úrokové náklady na leasing budovy                       |
| 801201                | Rozvaha | Zisk/ztráta - upravení leasingu                      |

## <a name="configure-posting-accounts"></a>Konfigurace účtů pro zaúčtování

Chcete-li přiřadit účty ke knihám a skupinám na leasing, musíte nakonfigurovat parametry pro leasing aktiv.

1. Přejděte do nabídky **Leasing majetku \> Nastavení \> Parametry zaúčtování leasingu**.
2. Na kartě **Účty** otevřete pevnou záložku **Leasingové účty**. Určete hlavní účty pro finanční a operativní leasing odpovídající **typu zaúčtování**. Předchozí tabulka ukazuje účty související s operativním a finančním leasingem.

    > [!NOTE]
    > Tento krok vyžaduje, abyste nastavili samostatné účty pro operativní i finanční leasing pro každý typ účtování kromě **Započtení nákladů na leasing** a **Zvýšení / snížení leasingu**. Společnosti, které dodržují účetní rámec IFRS 16, musí přidat hlavní účet pro operativní leasing. Systém ale tento účet nebude používat, i když je to povinné pole, protože všechny leasingy podle IFRS 16 jsou klasifikovány jako finanční leasingy.
    >[!NOTE]
    > **Zvýšení / snížení leasingu** bude použit jako typ zaúčtování pro další úvahy o majetku, včetně **Počáteční přímé náklady, leasingové pobídky, leasingové splátky a náklady na demontáž**, ale zaúčtuje se na hlavní účet aktiva s právem použití, který je výchozí pro **majetkový leasing**.        
    
3. Chcete-li vybrat konkrétní skupinu leasingu odpovídající hlavnímu účtu, v poli **Kód účtu** vyberte **Skupina**. Pak v poli **Číslo účtu / skupiny** vyberte skupinu leasingu, kterou chcete přiřadit k hlavnímu účtu.
4. Chcete-li přiřadit kódy účtu administrativním nákladům, které byly v systému nastaveny, na pevné záložce **zachraňovací náklady** v poli **Typ výdajů** vyberte výdaj. Poté pro každou knihu přiřaďte finanční a provozní účty.

    > [!NOTE]
    > Vybraný finanční nebo provozní účet bude odepsán po zaúčtování faktury za plánovaný výdaj.
    > **Vyrovnání výdajů na leasing** bude použito jako typ účtování pro transakce s náklady na výkon, ale zaúčtuje se na definovaný **Ofsetový účet** v **řádkách plánu plateb zachraňovacích nákladů** v podrobnostech leasingu nebo formuláři knihy leasingu.   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
