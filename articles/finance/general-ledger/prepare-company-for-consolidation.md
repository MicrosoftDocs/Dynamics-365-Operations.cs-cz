---
title: Připravit právnickou osobu pro proces konsolidace
description: Při konsolidaci shromáždíte transakce z několika sad účtů právnické osoby do jediné sady účtů právnické osoby. Toto téma vysvětluje, jak připravit právnickou osobu na konsolidaci.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 6f718bef3b1b07d3bb03dbf6acbf1cdf58aa7b8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815469"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>Připravit právnickou osobu pro proces konsolidace

[!include [banner](../includes/banner.md)]

Při konsolidaci shromáždíte transakce z několika sad účtů právnické osoby do jediné sady účtů právnické osoby. Toto téma vysvětluje, jak připravit právnickou osobu na konsolidaci.

> [!NOTE]
> Doporučujeme použít Management Reporter pro Microsoft Dynamics 365 Finance, chcete-li kombinovat finanční výsledky pro více právnických osob v konsolidovaném formátu. Management Reporter vám umožňuje vytvářet konsolidované finanční výkazy napříč právnickými osobami, používat Excel k importu konsolidačních dat z jiných zdrojů a převádět částky do libovolného počtu měn vykazování, aniž byste museli spouštět proces konsolidace v Dynamics 365 Finance.

Lze vytisknout sestavy, například finanční výkazy, z konsolidované právnické osoby. Konsolidovanou právnickou osobu však nelze použít pro denní transakce.

Můžete konsolidovat data z právnické osoby, která používá jiné databáze než konsolidovaná právnická osoba. Tento proces konsolidace je označován jako *konsolidace importu*. Právnické osoby mohou rovněž používat stejnou databázi jako konsolidovaná právnická osoba. Tento proces konsolidace je označován jako *online konsolidace.*

Konsolidovaná právnická osoba shromažďuje výsledky a zůstatky dceřiných společností. Při přípravě konsolidované právnické osoby ke konsolidaci je nutné postupovat takto.

1. Přejděte do části **Hlavní knika \> Nastavení \> Organizace \> Právnické osoby**.
2. Vyberte **Nová** a vytvořte právnickou osobu, která bude konsolidovanou právnickou osobou.
3. Zaškrtněte políčko **Použijte pro proces finanční konsolidace** a poté zadejte informace o konsolidované právnické osobě. Zadejte tento údaj přesně tak, jak se má zobrazovat na finančních výpisech konsolidované právnické osoby.
4. Zavřete stránku.
5. Vyberte konsolidovanou právnickou osobu v poli v pravém horním rohu stránky a poté vyberte **OK**.
6. Přejděte do části **Hlavní kniha \> Nastavení \> Hlavní kniha**.
7. Vyberte účtovou osnovu, fiskální kalendář, zúčtovací měnu, volitelnou měnu vykazování a výchozí typ směnného kurzu pro konsolidovanou právnickou osobu. 
8. Přejděte do části **Hlavní kniha \> Nastavení \> Měna \> Směnné kurzy**.
9. Nastavte směnné kurzy měny v relevantních obdobích pro měny dceřiných právnických osob.
10. Zavřete stránku.
11. Má-li konsolidovaná právnická osoba dceřiné společnosti, které používají cizí měny, postupujte takto:

    1. Přejděte do části **Hlavní kniha \> Nastavení \> Účtování \> Účty pro automatické transakce**.
    2. V poli **Typ zaúčtování** vyberte příslušný účet:

        - Pokud má právnická osoba zahraniční dceřiné společnosti, které jsou finančně nebo provozně závislé na mateřské právnické osobě, vyberte vhodný účet pro typ zaúčtování **Účet zisku a ztráty pro konsolidační rozdíly**.
        - Jestliže konsolidujete dceřinou společnost, která nezávisí finančně ani provozně na nadřazené právnické osobě, nebo právnickou osobu obsahující výsledky několika dceřiných společností, které nezávisí finančně ani provozně na nadřazené právnické osobě, a pokud používáte metody převodu ke konsolidaci dat, vyberte odpovídající účet pro typ zaúčtování **Protiúčet pro konsolidační rozdíly**.

    3. V poli **Hlavní účet** vyberte hlavní účty, které by se měly použít pro úpravy přecenění cizí měny.
    4. Zavřete stránku.

    Pokud vytvoříte konsolidovanou právnickou osobu na začátku období, je možné přecenit částky v cizí měně tak, jak se budou během období konsolidace měnit směnné kurzy.

Konsolidovaná právnická osoba je nyní nastavena pro periodickou úlohu **Konsolidace**. Můžete provést konsolidaci importu nebo konsolidaci online.

- Chcete-li provést konsolidaci importu, přejděte na **Hlavní kniha \> Periodické \> Konsolidace \> Konsolidace \[Importovat z\]**.
- Chcete-li provést online konsolidaci, přejděte na **Hlavní kniha \> Periodické \> Konsolidace \> Konsolidace \[Online\]**.

> [!NOTE]
> Před zpracováním konsolidace musíte připravit právnické osoby dceřiné společnosti na konsolidaci. Další informace viz [Založení dceřiné právnické osoby ke konsolidaci](set-up-subsidiary-company-for-consolidation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]