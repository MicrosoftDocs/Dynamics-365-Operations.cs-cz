---
title: Registrace příjmu vrácených položek
description: Příjem vráceného zboží můžete zaregistrovat pomocí formuláře Přehled doručení nebo Registrace.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a1dc18e50dd10568c719c4f87d805be526d6746
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576393"
---
# <a name="register-the-receipt-of-returned-items"></a>Registrace příjmu vrácených položek 

[!include [banner](../includes/banner.md)]


K dispozici jsou dva způsoby záznamu příjmu vrácených položek. Prvním způsobem je proces příjmu do skladu, který používá formulář **Přehled doručení**. Druhý používá formulář **Registrace**.

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a>Zaznamenat příjem vrácených položek ve formuláři Přehled doručení

Lze použít formulář **Přehled doručení** k identifikaci vrácené dodávky podle čísla autorizace vrácení materiálu (RMA). Pokud je definován název deníku na kartě **Nastavení** a řádky deníku, které odpovídají příslušným řádkům ve formuláři **Přehled doručení** existují, je vytvořeno nové záhlaví deníku po kliknutí na **Zahájit doručení**.

1.  Klikněte na **Řízení skladů** \> **Pravidelné** \> **Přehled příjezdů**.

2.  V poli **Název nastavení** vyberte **Vratka** a klikněte na **Aktualizovat**.
    

    > [!TIP]
    > <P>Výsledky hledání můžete omezit použitím polí <STRONG>Rozsah</STRONG>. Přesné výsledky dosáhnete zadáním nebo výběrem čísla RMA v poli <STRONG>číslo RMA</STRONG>. Pokud chcete definovat a uložit sadu filtrů, které budou omezovat, která příchozí doručení se zobrazí, klikněte na kartu <STRONG>nastavení</STRONG>. Dostupné filtry zahrnují typy skladů a překladiště.</P>

    

    > [!WARNING]
    > <P>Vrácené objednávky nelze směšovat s jinými typy doručení ve formuláři <STRONG>Přehled doručení</STRONG>. Proto bude odkaz vždy na prodejní objednávku, ale žádné ID prodejní objednávky nebude uvedeno v záhlaví deníku.</P>



3.  V mřížce **Příjmy** vyhledejte řádek, který odpovídá vracené položce a pak zaškrtněte políčko ve sloupci **Vybrat pro doručení**.

4.  Pokud chcete z vratky vyloučit určité řádky, například položky z původní objednávky, které nebyly obsaženy ve vratce, zrušte zaškrtnutí políček **Vybrat pro doručení** v tabulce **Řádky** v dolní části formuláře.

5.  Klikněte na tlačítko **Spustit doručení** a vytvořte deník doručení.
    

    > [!NOTE]
    > <P>Můžete vybrat několik vratek a zahrnout je do jednoho procesu doručení. Všechny řádky vratky budou zkopírovány do odpovídajícího řádku deníku pro doručení položek.</P>

    

    > [!NOTE]
    > <P>Deník doručení můžete vytvořit také ručně pomocí formuláře <STRONG>Doručení zboží</STRONG>. 



6.  Klikněte na **Řízení zásob** \> **Deníky** \> **Doručení položky** \> **Doručení položky**.

7.  Vyberte deník doručení, který jste právě vytvořili, a potom kliknutím na **Řádky** otevřete formulář **Řádky deníku, umístění**.

8.  Na kartě **Obecné** nastavte požadovanou hodnotu v poli **Množství**, pokud je to požadováno, a pak přiřaďte kód dispozice v poli **Kód dispozice**.
    
    Alternativně můžete vybrat políčko **Správa karantény**, chcete-li vrácené zboží odesílat prostřednictvím procesu kontroly v souvislosti s karanténním příkazem.
    

    > [!NOTE]
    > <P>Při odeslání vráceného zboží přes karanténu nelze zadat kód dispozice.</P>



9.  Klikněte na tlačítko **Ověřit**.

10. Pokud proces ověření proběhne bezchybně, klepněte na položku **Zaúčtovat**.

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a>Zaznamenat příjem vrácených položek ve formuláři Registrace

Jako alternativu k použití formuláře **Přehled doručení** můžete použít formulář **Registrace** pro registraci doručení vráceného zboží.

1.  Klikněte na **Prodej a marketing** \> **Společné** \> **Objednávky vratky** \> **Všechny objednávky vratky**. Vytvořte novou objednávku vratky nebo otevřete objednávku vratky ze seznamu. Na pevné záložce **Řádky** vyberte řádek vratky. Klikněte na **Aktualizovat řádek** a potom na **Registrace**.

2.  Přiřaďte kód dispozice v poli **Kód dispozice** a potom klikněte na tlačítko **OK**.
    

    > [!NOTE]
    > <P>Není možné odeslat položku ke kontrole jako karanténní objednávku pomocí formuláře <STRONG>Registrace</STRONG>.</P>



3.  V mřížce **Transakce** vyberte transakci, která má být zaregistrována.

4.  V mřížce **registrovat** klepněte na tlačítko **přidat**. Opakujte předchozí dva kroky, dokud se všechny vrácené položky nezobrazí v mřížce **Registrovat**.

5.  Klikněte na **Zaúčtovat vše**.

## <a name="see-also"></a>Viz také

[Přehled doručení (formulář)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]