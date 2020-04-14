---
title: Převod rozpočtů projektu na konci fiskálního roku
description: Tento článek obsahuje informace, jak převést zbývající částky rozpočtu do budoucích let a vytvořit podrobnosti o registru rozpočtu.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172323"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Převod rozpočtů projektu na konci fiskálního roku

[!include [banner](../includes/banner.md)]

Při práci na projektu na více let můžete mít na konci fiskálního roku zbývající rozpočet. Můžete převést zbývající částky rozpočtu do budoucího roku a vytvořit podrobnosti registru rozpočtu daných částek v přidružených účtech hlavní knihy. Dříve než převedete zbývající částky do dalšího období, zkontrolujte a analyzujte zbývající částky rozpočtu.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Kontrola a analýza zbývajících částek rozpočtu

Proveďte následující kroky, pokud chcete zkontrolovat částky rozpočtu pro projekty na konci roku, ale nechcete částky převést do dalšího období.

1. Přejděte na **Řízení projektů a účetnictví** > **Periodicky** > **Rozpočty** > **Převést rozpočty do dalšího období**. 
2. Na stránce **Proces převedení projektového rozpočtu do dalšího období** ověřte na kartě **Možnosti na konci roku**, že není povolena možnost **Převést do dalšího období zbývající částky rozpočtu projektu**.
3. Na kartě **Parametry** v poli **Rozpočtový rok projektu** vyberte fiskální rok, pro který chcete zobrazit zbývající částku rozpočtu. 
4. V poli **Počáteční fiskální rok** vyberte fiskální rok, pro který chcete zobrazit zbývající částku rozpočtu. 
5. V poli **Z modelu prognózy** vyberte možnost **Zbývající rozpočet**. 
6. Chcete-li zahrnout projekty, které vyhovují vybraným kritériím a nemají žádný zbývající rozpočet,vyberte **Zobrazit nulový zůstatek**.  
7. Na kartě **Výběr rozpočtů** vyberte možnost **Načíst všechny rozpočty**, chcete-li načíst všechny rozpočty, které odpovídají vybraným kritériím, a poté vyberte možnost **Zpracovat**. 
8. Chcete-li navrhnout databázový dotaz, který načte určitou sadu rozpočtů do podokna, vyberte možnost **Načíst vybrané rozpočty**.

Chcete-li získat další informace o konkrétním řádku v podokně, vyberte daný řádek a pak vyberte možnost **Zobrazit podrobnosti rozpočtu** nebo **Zobrazit účty**.

## <a name="carry-forward-remaining-budget-amounts"></a>Převedení zbývajících částek rozpočtů do dalšího období 

Při zpracování zbývajících částek rozpočtů můžete vytvořit transakce v hlavní knize pro částky, které chcete převést do dalšího období. Chcete-li vytvořit transakce hlavní knihy, proveďte kroky v sekci [Převést částky rozpočtu do dalšího období a vytvořit transakce hlavní knihy](#carry-forward). 

> [!NOTE]
> Částky rozpočtů, které se převádějí do dalšího období, jsou převedeny do modelu prognózy, který je vybrán na stránce **Modely prognózy** jako model prognózy pro převod do dalšího období.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Převést částky rozpočtu do dalšího období a vytvořit transakce hlavní knihy

1.  Vyberte **Řízení projektů a účetnictví** > **Periodicky** > **Rozpočty** > **Převést rozpočty do dalšího období**. 
2. Na stránce **Proces převedení projektového rozpočtu do dalšího období** vyberte **Konec roku** a poté povolte možnosti **Převést do dalšího období zbývající částky rozpočtu projektu** a **Vytvořit položky registru rozpočtu v hlavní knize**. 
3. Na kartě **Parametry** ve skupině polí **Parametry projektu** vyberte následující možnosti:

   - **Rozpočtový rok projektu**: Vyberte začátek fiskálního roku, pro který chcete zobrazit zbývající částky rozpočtu. 
   - **Zisk a ztráta**: Vytvoření transakcí zisku a ztráty v hlavní knize. 
   -  **NV**: Vytvoření transakcí nedokončené výroby (NV) v hlavní knize.
   -  **Mzdy**: Vytvoření transakcí přidělování mezd v hlavní knize. 

5. Do skupiny polí **Hlavní kniha** zadejte následující informace: 

   - V poli **Počáteční fiskální rok** vyberte fiskální rok, do kterého chcete přenést zbývající částky rozpočtu pro projekty. Výchozí hodnota je jeden rok po hodnotě v poli **Rozpočtový rok projektu**.
   -  V poli **Období převedení do dalšího období** vyberte období, pro které chcete vytvořit podrobnosti registru rozpočtu v hlavní knize. To je obvykle první období v počátečním fiskálním roce.

6. Do skupiny polí **Kopírovat z/do** zadejte následující informace:

   - V poli **Z modelu prognózy** vyberte model prognózy rozpočtu projektu přidružený ke zbývajícím částkám rozpočtů, které chcete převést pro projekty. 
   - V poli **Do rozpočtového modelu hlavní knihy** vyberte model rozpočtu hlavní knihy přidružený ke zbývajícím částkám rozpočtů, které chcete převést do hlavní knihy. 
   -  Chcete-li použít prodejní měnu projektu pro transakce hlavní knihy, které jsou vytvořeny při převodu částek rozpočtu pro projekty, vyberte možnost **Převést prodejní měnu**. Pokud možnost není vybrána, budou transakce používat zúčtovací měnu. 
   -  Pokud chcete zahrnout projekty bez zbývajících částek rozpočtu, které ale splňují ostatní kritéria vybraná v projektech zobrazených ve spodním podokně, vyberte možnost **Zobrazit nulový zůstatek**.

7. Na kartě **Výběr rozpočtů** vyberte možnost **Načíst všechny rozpočty**, chcete-li načíst všechny rozpočty, které odpovídají vybraným kritériím. Pokud chcete navrhnout databázový dotaz, který načte určitou sadu rozpočtů projektu do podokna, vyberte možnost **Načíst vybrané rozpočty**.
8. Pro každý projekt, který chcete zpracovat, vyberte možnost na začátku řádku projektu.

    > [!TIP]
    > Chcete-li vybrat všechny nebo většinu projektů, zaškrtněte políčko v horním levém horním rohu. Chcete-li vyloučit zpracování libovolného projektu, zrušte zaškrtnutí u daného projektu.

9. Chcete-li převést zbývající částky rozpočtu pro vybrané projekty do vybraného fiskálního roku a vytvořit podrobnosti registru rozpočtu v hlavní knize, vyberte možnost **Zpracovat**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Převedení částek rozpočtů do dalšího období bez vytvoření transakcí hlavní knihy

1. Přejděte na **Řízení projektů a účetnictví** > **Periodicky** > **Rozpočty** > **Převést rozpočty do dalšího období**.
2. Na stránce **Proces převedení projektového rozpočtu do dalšího období** vyberte na kartě **Možnosti na konci roku** možnost **Převést do dalšího období zbývající částky rozpočtu projektu**.
3. Ve skupině **Parametry** v poli **Rozpočtový rok projektu** vyberte fiskální rok, pro který chcete zobrazit zbývající částky rozpočtu.
4. Ve skupině **Kopírovat z/do** zadejte následující informace:

   - V poli **Z modelu prognózy** vyberte model prognózy rozpočtu projektu, který je spojen se zbývajícími částkami rozpočtu, které chcete převést pro projekty. 
   - Vyberte **Zobrazit nulový zůstatek**, chcete-li zahrnout projekty, které nemají žádné zbývající částky rozpočtu, ale vyhovují vybraným kritériím.
   - Ve skupině **Výběr rozpočtů** vyberte možnost **Načíst všechny rozpočty**, chcete-li načíst všechny rozpočty, které odpovídají vybraným kritériím. Chcete-li navrhnout databázový dotaz, který načte určitou sadu rozpočtů projektu do podokna, vyberte možnost **Načíst vybrané rozpočty**.

5. Pro každý projekt, který chcete zpracovat, vyberte možnost na začátku řádku projektu. 
6. Možností **Zpracovat** převedete zbývající částky rozpočtu pro vybrané projekty do vybraného fiskálního roku.

