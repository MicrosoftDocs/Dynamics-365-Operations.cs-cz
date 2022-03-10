---
title: Zásobování
description: Tohle téma popisuje zásobování v modulu Správa majetku.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderPurchaseListPagePreviewPane, EntAssetWorkOrderPurchaseListPage, EntAssetWorkOrderPurchaseLineAmountInfoPart, EntAssetWorkOrderPurchReqListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2b5e160beb4743db2530b91020f21b686d84237b17cfa7ff7f0cc1da97695d08
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743643"
---
# <a name="procurement"></a>Zásobování

[!include [banner](../../includes/banner.md)]

V modulu Správa majetku můžete získat přehled o nákupních žádankách a nákupních objednávkách souvisejících s pracovními příkazy. Je rovněž možné vytvořit nákupní objednávku nebo nákupní žádanku z pracovního příkazu.

Na stránce se seznamem **Nákupní žádanky na pracovním příkazu** (**Správa majetku** > **Společné** > **Zásobování** > **Nákupní žádanka na pracovním příkazu**) se zobrazuje seznam nákupních žádanek souvisejících s pracovními příkazy. Když na této stránce vyberete úlohu pracovního příkazu, můžete použít tlačítka ve skupině **Zobrazit** na kartě podokna akcí **Nákupní žádanka pracovního příkazu** k provádění různých akcí:

- Chcete-li otevřít související nákupní žádanku, vyberte možnost **Nákupní žádanka**. 
- Chcete-li otevřít související pracovní příkaz, vyberte možnost **Pracovní příkaz**.
- Chcete-li získat přehled o tom, kde se ve správě majetku používá položka na vybraném řádku, ve vztahu k majetku, výchozím typům práce, náhradním dílům a pracovním příkazům, vyberte **Položka, kde se používá**. Další informace o tomto přehledu naleznete v tématu [Položka, kde se používá](../controlling-and-reporting/item-where-used.md)se používá.

Na následujícím obrázku je uveden příklad stránky se seznamem **Nákupní žádanka pracovního příkazu**.

![Obrázek č. 1.](media/08-work-orders.png)


Na stránce se seznamem **Nákupní v pracovním příkazu** (**Správa majetku** > **Společné** > **Zásobování** > **Nákupní v pracovním příkazu**) se zobrazuje seznam nákupních objednávek souvisejících s pracovními příkazy. Když na této stránce vyberete úlohu pracovního příkazu, můžete použít tlačítka ve skupině **Zobrazit** na kartě podokna akcí **Nákupní objednávka pracovního příkazu** k provádění různých akcí:

- Chcete-li otevřít související nákupní objednávku, vyberte možnost **Nákupní objednávka**. 
- Chcete-li otevřít související pracovní příkaz, vyberte možnost **Pracovní příkaz**.
- Chcete-li získat přehled o tom, kde se ve správě majetku používá položka na vybraném řádku, ve vztahu k majetku, výchozím typům práce, náhradním dílům a pracovním příkazům, vyberte **Položka, kde se používá**. Další informace o tomto přehledu naleznete v tématu [Položka, kde se používá](../controlling-and-reporting/item-where-used.md)se používá.

Na následujícím obrázku je uveden příklad stránky se seznamem **Nákup pracovního příkazu**.

![Obrázek č. 2.](media/09-work-orders.png)


Na stránce se seznamem **Nákup pracovního příkazu** a na stránce se seznamem **Nákupní žádanka pracovního příkazu** se zobrazí symbol související s ovládacím prvkem data doručení, a to na pravé straně každého řádku. Pokud má ikona podobu vykřičníku v červeném kruhu, znamená to, že dodávka v související nákupní žádance nebo nákupní objednávce může být zpožděna.

Pro nákupní objednávku se použije datum související s řádkem nákupní objednávky k výpočtu možného zpoždění. Chcete-li zobrazit toto datum, vyberte na stránce **Nákupní objednávka** řádek nákupní objednávky. Toto datum je uvedeno v poli **Potvrzené datum dodání** na kartě **Nastavení** pevné záložky **Podrobnosti žádku**. Pokud není nastaveno pole **Potvrzené datum dodání**, bude pro výpočet použito datum uvedené v poli **Datum dodání** na pevné záložce **Záhlaví nákupní objednávky**. Jedno z těchto dat se porovnává s dostupným datem na pracovním příkazu nebo na úloze pracovního příkazu v následujícím pořadí:

1. Skutečné datum zahájení na pracovním příkazu  

2. Naplánované datum zahájení na související úloze pracovního příkazu 

3. Naplánované datum zahájení na pracovním příkazu 

4. Očekávané datum zahájení na pracovním příkazu nebo 

Datum v poli **Požadované datum** u nákupní žádanky na pevné záložce **Záhlaví nákupní objednávky** na stránce **Nákupní žádanky** slouží k výpočtu možného zpoždění. Datum v tomto poli se porovnává s dostupným datem v pracovním příkazu nebo v úloze pracovního příkazu ve stejném pořadí jako datum nákupní objednávky.


## <a name="create-a-purchase-order-from-a-work-order"></a>Vytvoření nákupní objednávky z pracovního příkazu

Na stránce se seznamem **Všechny pracovní příkazy** můžete vybrat úlohu pracovního příkazu a pak vytvořit související nákupní objednávku nebo nákupní žádanku. Tímto způsobem pomáháte zaručit, že existují vztahy projektů mezi nákupní objednávkou nebo nákupní žádankou a pracovním příkazem.

1. Vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz, pro který chcete vytvořit nákupní objednávku, a pak vyberte možnost **Upravit**.

3. Na pevné záložce **Práce údržby na pracovním příkazu** vyberte úlohu pracovního příkazu, pro kterou chcete vytvořit nákupní objednávku.

4. Vyberte **Úlohy položky** > **Nákupní objednávka na základě úlohy pracovního příkazu**.

5. Na stránce se seznamem **Nákupních objednávek projektu** klikněte na položku **Nová**.

6. Vytvořte nákupní objednávku.

>[!NOTE]
>Chcete-li vytvořit související nákupní žádanku, postupujte stejným způsobem. V kroku 4 věak vyberte **Úlohy položky** > **Nákupní žádanka z úlohy pracovního příkazu**.


## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Vztah projektu mezi pracovním příkazem a nákupní objednávkou nebo nákupní žádankou

Řádek nákupní objednávky nebo řádek nákupní žádanky souvisí s úlohou pracovního příkazu pomocí projektu pracovního příkazu a souvisejícím číslem aktivity projektu. Při vytvoření nákupní objednávky nebo nákupní žádanky z úlohy pracovního příkazu je číslo související aktivity projektu povinné. Pokud mají všechny úlohy pracovního příkazu v souvisejícím pracovním příkazu stejný typ práce údržby, číslo aktivity projektu je automaticky zadáno do nákupní objednávky nebo nákupní žádanky. Pokud mají úlohy pracovního příkazu různé typy práce údržby, musíte ručně zadat číslo aktivity projektu do nákupní objednávky nebo nákupní žádanky.

Chcete-li zobrazit nebo zadat číslo aktivity související s řádkem nákupní objednávky, na stránce se seznamem **Nákup pracovního příkazu** vyberte záznam nákupní objednávky a pak ve sloupci **Nákupní objednávka** vyberte odkaz na nákupní objednávku. Pole **Číslo aktivity** najdete na kartě **Projekt** pevné záložky **Podrobnosti řádku**.

Následující obrázek ukazuje příklad stránky **Nákupní objednávka** se zaměřením na **číslo aktivity**.

![Obrázek č. 3.](media/10-work-orders.png)

Podobně platí, že chcete-li zobrazit nebo zadat číslo aktivity související s řádkem nákupní žádanky pracovního příkazu, na stránce se seznamem **Nákup pracovního příkazu** vyberte záznam nákupní objednávky a pak ve sloupci **Nákupní žádanka** vyberte odkaz na nákupní žádanku. Pole **Číslo aktivity** najdete na kartě **Projekt** pevné záložky **Podrobnosti řádku**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]