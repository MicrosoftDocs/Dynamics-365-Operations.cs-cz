---
title: "Nákladová cena vrácení a ID vrácené šarže"
description: "Můžete chtít, aby se náklady na vrácené produkty rovnaly nákladům na produkty v době, kdy jste produkty prodali zákazníkovi. To lze provést pomocí **ID vrácené šarže**."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: aeba56128ab6c9ab7d244bdf153faba8e96069d6
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="return-cost-price-and-return-lot-id"></a>Nákladová cena vrácení a ID vrácené šarže        

[!include [banner](../includes/banner.md)]



Náklady na produkty, které byly vráceny do zásob, se vypočítávají s použitím aktuálních nákladů produktů. Můžete však požadovat, aby se náklady na vrácené produkty rovnaly nákladům na produkty v době, kdy jste produkty prodali zákazníkovi. To lze provést pomocí **ID vrácené šarže** na pevné záložce **Podrobnosti řádku** ve formuláři **prodejní objednávka**.

Představte si například následující příklady: Vystavíte fakturu odběrateli. Pak vám odběratel vrátí dodané produkty. Vrátíte produkty do zásob. V takovém případě, když odběrateli účtujete vrácené produkty, jsou náklady na tyto produkty vypočteny s použitím aktuálních nákladů na produkty. Pokud však použijete pole **ID vrácené šarže**, jsou náklady na vracené výrobky vypočteny s použitím nákladů na faktuře původního prodeje odběrateli.

Chcete-li použít jiné než aktuální náklady za zboží vrácené od odběratele, použijte některou z následujících metod.

## <a name="method-1-manually-enter-the-return-cost-price"></a>Metoda č. 1: Ručně zadejte náklady na vrácení

Ve výchozím nastavení při přidání položky do vratky budou položky vráceny do zásob s aktuální nákladovou cenou. Při určení jiné ceny nákladů vrácení postupujte takto.

1.  Klikněte na **Prodej a marketing** \> **Společné** \> **Objednávky vratky** \> **Všechny objednávky vratky**.

2.  V **podokně akcí** ve skupině **Nový** klepněte na možnost **Vratka**.

3.  Ve formuláři **Vytvořit vratku** vyberte účet zákazníka a klepněte na tlačítko **OK**.

4.  Ve formuláři **vratka – číslo RMA: %1, %2** vyberte položku a poté zadejte záporné množství do pole **množství**.

5.  Klikněte na pevnou záložku **Podrobnosti řádku**.

6.  Na kartě **Obecné** zadejte hodnotu v poli **Upřednostňovaný kalendář**. Tato hodnota se používá při vrácení zboží do zásob. Pokud nezadáte hodnotu, aktuální nákladová cena je použita při vrácení zboží do zásob.

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a>Metoda č. 2: Automatické generování nákladové ceny na základě řádku faktury odběratele

Toto je preferovaná metoda používaná k vytvoření řádků vratky. Pokud chcete použít náklady na produkty v době prodeje produktů odběrateli, vytvořte vratku a zadejte řádku prodeje do vratky.

1.  Klikněte na **Prodej a marketing** \> **Společné** \> **Objednávky vratky** \> **Všechny objednávky vratky**.

2.  V **podokně akcí** ve skupině **Nový** klepněte na možnost **Vratka**.

3.  Ve formuláři **Vytvořit vratku** vyberte účet zákazníka a klepněte na tlačítko **OK**.

4.  Ve formuláři **vratka – číslo RMA: %1, %2** v **podokně akcí** klepněte na tlačítko **najít prodejní objednávku**.

5.  Ve formuláři **najít prodejní objednávku** vyberte řádek faktury k vrácení a klepněte na tlačítko **OK**.
    
    Na pevné záložce **podrobnosti řádku** na kartě **Obecné** se v poli **ID vrácené šarže** zobrazí hodnota z původní řádky objednávky. V poli **náklady na vrácení** se dále zobrazí hodnot nákladů z původní řádky prodejní objednávky.

## <a name="cost-calculation-example"></a>Příklad výpočtu nákladů

Používáte-li pole **ID vrácené šarže** na řádku objednávky k určení nákladů na vrácení, použijí se náklady řádku objednávky. Pokud spustíte funkci uzávěrky nebo přepočtu skladu, náklady se upraví na řádku původní prodejní objednávky. Náklady řádku objednávky se automaticky nastaví tak, aby odrážely stejnou cenu za kus.

1.  Vytvořte a vydejte produkt s názvem test. Ve formuláři **uvolnění podrobností produktu** zadejte následující informace:
    
    1.  Na pevné záložce **řízení nákladů** v poli **skupinu položek** vyberte skupinu **části**.
    
    2.  Na pevné záložce **Obecné**, v poli **Skupina modelů položky** vyberte **DEF**.
    
    3.  Na pevné záložce **Nákup** v poli **cena** zadejte 10,00 jako nákladovou cenu položky.
    
    4.  V **podokně akcí** klikněte na možnost **Skupiny dimenze**. V poli **Skupina dimenze úložiště** vyberte **Pouze pracoviště a sklad**. V poli **Skupina sledovací dimenze** vyberte **Žádné aktivní sledovací dimenze**.

2.  Vytvořte nákupní objednávku pro 10 kusů zkušební položky po 6,00 za kus a potom zaúčtujte faktury pro nákupní objednávku.
    
    Vytvořte druhou nákupní objednávku pro 10 kusů zkušební položky po 8,00 za kus a potom zaúčtujte faktury pro nákupní objednávku.

3.  Zaúčtujte fakturu prodejní objednávky na prodej pěti kusů zkušební položky.
    
    V takovém případě jsou na řádku prodejní objednávky vypočítány náklady na 35,00 (5 kusů \*7,00 průměrné náklady na úkolové práce).

4.  Vytvořte novou vratku pro vybraného odběratele. Ve formuláři **najít prodejní objednávku** vyberte řádek faktury a klepněte na tlačítko **OK**.

5.  Ve formuláři **vratka – číslo RMA: %1, %2** ověřte, že vratka je vygenerována pro vrácení testovacího zboží. Množství vratky je nastaveno na hodnotu -5,00.
    
    Pole **ID vrácené šarže** zobrazí ID šarže. Toto ID šarže je převzato z původní prodejní objednávky položky, která byla prodána zákazníkovi. V poli **náklady na vrácení** se dále zobrazí nákladová cena z původní řádky prodejní objednávky.

6.  Zaregistrujte příjem vrácených položek.

7.  Zaúčtujte dodací list pro vrácené položky.

8.  Zaúčtujte fakturu pro objednávku vratky. Na stránce se seznamem **všechny prodejní objednávky** vyberte požadovanou prodejní objednávku, pro kterou je typ objednávky **vratka**.

9.  Otevřete formulář **Skladové transakce**. Ověřte, že je vratka účtována na 7,00 za kus pomocí hodnoty v poli **Náklady na vrácení**, za celkem 35,00 v poli **částka nákladů**. Můžete otevřít formulář **skladové transakce** z formuláře **vratka – číslo RMA: %1, %2**. V mřížce **Řádky** klikněte na **Sklad** \> **Transakce**.

10. V modulu Řízení zásob a skladu použijte formulář **závěrka a oprava** a spusťte formulář ke spuštění **3. závěrky**.
    
    Tato akce, nastaví náklady pro původní řádek prodeje, který byl vypočítán při -35,00 (5 kusů \* 7,00) k -30,00 (5 kusů \* 6,00). Je to proto, že skupina skladových modelů používá metodu první do skladu, první ze skladu (FIFO), a náklady 6,00 za kus z první nákupní objednávky. Kromě toho tato akce upraví náklady na vrácení řádku prodeje tak, aby odpovídal ceně za kus v původním řádku nákupní objednávky. Proto náklady řádku vrácenky budou upraveny z 35,00 na 30,00.





