---
title: Vytvoření objednávky náhrady položky
description: Objednávky náhrady položek jsou obvykle vytvořeny po vrácení a kontrole výrobku.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e63c175d12cac91648cb57a3f41d1769e81d57af
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424005"
---
# <a name="create-an-item-replacement-order"></a>Vytvoření objednávky náhrady položky 

[!include [banner](../includes/banner.md)]


Objednávky náhrady položek jsou obvykle vytvořeny po vrácení a kontrole výrobku. Pokud je však nutné položku nahradit ještě před vrácením nebo pokud původní položka nebude vrácená, můžete vytvořit objednávku náhrady bezprostředně po vytvoření vratky.

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>Vytvořit objednávku náhrady po přijetí vráceného zboží

1.  Klikněte na **Prodej a marketing** \> **Společné** \> **Objednávky vratky** \> **Všechny objednávky vratky**.

2.  Vytvořte novou objednávku vratky nebo vyberte objednávku vratky ze seznamu a otevřete formulář **Vratka - číslo RMA: %1, %2**.

3.  Klepněte na tlačítko **řádek vratky** a poté vyberte **náhradní součást**.

4.  Vyberte položku, kterou chcete nahradit vrácené zboží. Zadejte specifikace položky a klikněte na tlačítko **Použít**.

5.  Klikněte na **Dodací list** k vygenerování dodacího listu pro objednávku vratky. Prodejní objednávka je generována pro náhradní zboží, které jste vybrali.
    
    Po vytvoření prodejní objednávky náhradního zboží jsou prodejní smlouvy automaticky prohledány, a pokud existuje příslušná prodejní smlouva, je použita na prodejní objednávku.

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>Vytvoření objednávky náhrady dříve, než je přijata vracená položka

1.  Klikněte na **Prodej a marketing** \> **Společné** \> **Objednávky vratky** \> **Všechny objednávky vratky**.

2.  Vytvořte novou vratku nebo vyberte vratku ze seznamu a otevřete formulář **Vratka - číslo RMA: %1, %2**.

3.  Klikněte na **Najít prodejní objednávku**, pokud chcete identifikovat prodejní objednávku pro vrácenou položku. Vyplňte formulář **Najít prodejní objednávku** a kliknutím na **OK** zavřete formulář a vraťte se do formuláře **Vratka – číslo RMA:%1, %2**. Řádek prodejní objednávky pro vrácené zboží se zkopíruje do objednávky vratky.

4.  Klepněte na tlačítko **náhradní objednávka** pro otevření formuláře **Vytvořit prodejní objednávku**.

5.  Zaškrtnutím políčka **Kopírovat řádky vratek** přesuňte podrobnosti z vratky vybrané ve formuláři **Vratka – číslo RMA:%1, %2** do této prodejní objednávky.

6.  Podle potřeby zadejte nebo upravte podrobné údaje.
    
    Pokud jste identifikovali v kroku 3 prodejní objednávku, a pokud je řádek prodejní objednávky pro vrácené zboží spojen s prodejní dohodou, identifikátor platné prodejní smlouvy pro objednávku náhradního zboží se automaticky zobrazí v poli **ID prodejní objednávky**.

7.  Klikněte na tlačítko **OK**, zavřete formulář **Vytvořit prodejní objednávku** a otevřete formulář **Prodejní objednávka**, kde můžete pokračovat k zadání informací pro novou prodejní objednávku. Všechny řádky platné objednávky vratky budou zkopírovány do nové prodejní objednávky. 
    
    Je-li identifikátor prodejní smlouvy automaticky zobrazen v poli **ID prodejní smlouvy**, pak prodejní smlouvu byla spojena se záhlavím prodejní objednávky náhradního zboží. Pokud je v prodejní smlouvě platný závazek, který ještě nebyl naplněn, a prodejní objednávka je vytvořena před vypršením platnosti prodejní smlouvy, je vytvořeno propojení mezi řádkem prodejní smlouvy a řádkem prodejní objednávky. Proto se informace z prodejní smlouvy, jako je cena zboží, zkopíruje do nového řádku prodejní objednávky. 
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]