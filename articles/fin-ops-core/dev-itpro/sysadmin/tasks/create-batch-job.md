---
title: Vytvoření dávkové úlohy
description: Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS).
author: maertenm
ms.date: 11/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76c6c68f7effad0c40282b22ea2a6bf991862cf5
ms.sourcegitcommit: d7d997ad84623ad952672411c0eb6740972ae0b1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/24/2021
ms.locfileid: "7864166"
---
# <a name="create-a-batch-job"></a>Vytvoření dávkové úlohy

[!include [banner](../../includes/banner.md)]

Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS). Dávkové úlohy jsou spouštěny s bezpečnostním pověřením uživatele, který je vytvořil. Dávkovou úlohu můžete nastavit následujícím postupem. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-the-batch-job"></a>Vytvoření dávkové úlohy
1. Přejděte do **navigačního podokna > Moduly > Správa systému > Dotazy > Dávkové úlohy**.
2. Zvolte **Nové**.
3. Do pole **Popis úlohy** zadejte popis dávkové úlohy.
4. Do pole **Datum/čas plánovaného zahájení** zadejte datum a čas, kdy se má dávková úloha spustit.
5. Zvolte možnost **Uložit**.

## <a name="create-a-recurrence"></a>Vytvoření opakování
1. V podokně akcí vyberte **Dávková úloha**.
2. Vyberte **Opakování**. Pomocí těchto možností zadejte rozsah a vzor opakování.  
3. Vyberte **OK**.

## <a name="add-alerts"></a>Přidání výstrah
1. V podokně akcí vyberte **Dávková úloha**.
2. Vyberte **Upozornění**. Určete, zda chcete odeslat upozornění po dokončení dávkové úlohy, dojde-li k chybě nebo dojde ke zrušení. Poté stanovte, zda chcete, aby se výstrahy zobrazily v místním okně.   
3. Vyberte **OK**.

## <a name="add-a-task-to-a-batch-job"></a>Přidání úkolu do dávkové úlohy
1.  Na stránce **Dávkové úlohy** vyberte možnost **Zobrazit úkoly**.
2.  Vyberte **Ctrl+N** a vytvořte úkol.
3.  Zadejte popis dávkové úlohy.
4.  V poli **Firemní účty** vyberte databázi společnosti, ve které má být úloha spuštěna.
5.  V poli **Název třídy** vyberte proces, který má úkol spustit. 
6.  Podle potřeby vyberte skupinu dávek pro úlohu.

    Klientské úkoly musejí být přiřazeny do dávkové skupiny. Jsou automaticky přiřazeny k výchozí dávkové skupině (také známé jako Prázdná dávková skupina).

7.  Vybrat **Ctrl+S** pro uložení úkolu.
8.  Chcete-li, aby byl vybraný úkol závislý na jiném úkolu v úloze, vyberte mřížku **Má podmínky** poté pro každou podmínku, kterou chcete definovat, postupujte takto:

    1. Vyberte **Ctrl+N** a vytvořte podmínku.
    2. Vyberte ID nadřazeného úkolu.
    3. Vyberte stav nadřazeného úkolu, kterého musí být dosaženo před spuštěním závislého úkolu.
    4. Vybrat **Ctrl+S** pro uložení podmíky.

    Jestliže definujete víc než jednu podmínku a pokud *všechny* podmínky musejí být před spuštěním závislého úkolu splněny, vyberte typ **všechny**. Má-li být závislý úkol spuštěn, pokud je slněna *libovolná* podmínka, vyberte typ podmínky **libovolná**.

9.  Vyberte, jak se mají řešit selhání úloh. Chcete-li ignorovat selhání konkrétního úkolu, na kartě **Všeobecné** vyberte možnost **Ignorovat selhání úlohy** pro daný úkol. Pokud je tato možnost vybrána, pak selhání úkolu nezpůsobí selhání celé úlohy. Také můžete použít políčko **Maximální počet opakování** a upřesnit počet pokusů o opakované spuštění úkolu, než dojde k selhání. Jako osvědčený postup doporučujeme nenastavovat pole **Maximální počet opakování** na hodnotu, která je větší než **5**.

    Další informace o dávkových opakováních viz [Povolit dávkové opakování](../retryable-batch.md).

## <a name="adjust-batch-job-status"></a>Úprava stavu dávkové úlohy
1. Přejděte na **Správa systému > Dotazy > Dávkové úlohy**.
2. Vyberte odpovídající dávkovou úlohu.
3. V podokně akcí vyberte **Dávková úloha > Funkce > Změnit stav**.
4. Vyberte příslušný stav:
    - **Srážka**: Nastavte dávkovou úlohu jako **srážku** tak, aby byla zadržena plánovačem dávkových úloh. Ekvivalent *zastavení*
    - **Čekání**: Nastavte dávkovou úlohu jako **čekání**, aby čekala na vyzvednutí plánovačem úloh. Ekvivalent *přejít*
5. Vyberte **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
