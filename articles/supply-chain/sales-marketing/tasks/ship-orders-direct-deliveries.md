---
title: Expedování objednávek jako přímých dodávek
description: Toto téma ukazuje, jak vytvořit přímé dodávky pro prodejní objednávku.
author: omulvad
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart, PurchEditLines, PurchTable, PurchTableReferences, MCRDropShipWorkbench, SalesShippingLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5488ac6d29a99bcaa5ea29ea6da131858070011c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824791"
---
# <a name="ship-orders-as-direct-deliveries"></a>Expedování objednávek jako přímých dodávek

[!include [banner](../../includes/banner.md)]

Toto téma ukazuje, jak vytvořit přímé dodávky pro prodejní objednávku. Přímou dodávku používejte, pokud chcete zboží expedovat odběrateli přímo od dodavatele, místo expedice nejprve do svého vlastního skladu,. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. K úspěšnému dokončení druhého podúkolu „Vytvoření přímé dodávky z pracovní plochy“ se ujistěte, že zboží, která vyberete v prodejní objednávce, má určeného výchozího dodavatele na pevné kartě Nákup vydaného základního produktu.

## <a name="set-an-individual-order-for-direct-delivery"></a>Nastavení jednotlivé objednávky pro přímé dodání
1. Přejděte na **Navigační podokno > Moduly > Pohledávky > Objednávky > Všechny prodejní objednávky**.
2. Zvolte **Nové**.
3. Zadejte nebo vyberte hodnotu v poli **Účet odběratele** a pak vyberte **OK**
4. Zadejte nebo vyberte hodnoty v polích **Číslo položky** a **Pracoviště** a pak vyberte možnost **Uložit**.
5. V podokně akcí vyberte **Prodejní objednávka** a pak **Přímá dodávka**. Vytvoření seznamů stránek dodávek všech otevřených řádků prodejních objednávek jako kopírovaných z prodejní objednávky. Můžete zkontrolovat podrobnosti o objednávce, a v případě potřeby můžete upravit podrobnosti jako například nákupní množství a podmínek cen předtím, než vytvoříte přímou dodávku.  
6. Vyberte možnost **Ano** v poli **Zahrnout vše**.
    - Pokud chcete generovat přímou dodávku pouze pro podmnožinu řádků prodejních objednávek, vyberte je jednotlivě.  
    - Pole **Účet dodavatele** může nebo nemusí být vyplněno číslem dodavatele. Pokud bude výchozí dodavatele nastaven pro produkt (v přidružené disponibilitě položky), pak do řádku bude zkopírován tento dodavatel. V ostatních případech musíte dodavatele zadat ručně. V tomto příkladu vybereme nového dodavatele v dalším kroku i v případě, že jeden je již vyplněn.   
7. Zadejte nebo vyberte hodnotu v poli **Účet dodavatele** a pak vyberte **OK**. Zpráva vás informuje o tom, že nákupní objednávka nyní byla vytvořena.   
8. Rozbalte sekci **Podrobnosti řádku**.
9. Vyberte kartu **Dodávka** a ověřte, že pole **Přímá dodávka** je nastaveno na hodnotu **Ano**.
10. V podokně akcí klikněte na možnost **Obecné**.
11. Vybrat **Související objednávky**.
12. Vyberte odkaz v poli **Nákupní objednávka**.
13. Rozbalte oddíl **Podrobnosti řádku** a vyberte kartu **Adresa**.
    - Doručovací adresa pro tento řádek nákupní objednávky je adresa dodání odběratele, a nikoli adresa vaší společnosti.  
    - Pokud upravíte adresu dodání na řádku prodejní objednávky nebo na řádku původní nákupní objednávky, bude adresa automaticky aktualizována na řádku odpovídající objednávky.  
14. Vyberte kartu **Dodávka**.
    - Stejně jako řádek prodejní objednávky je typ řádku přidružené nákupní objednávky také nastaven na přímou dodávku.  
    - Datum dodání na řádku nákupní objednávky a potvrzené datum dodání jsou v uvedeném pořadí nastaveny k požadovanému datu příjmu a potvrzenému datu příjmu původního řádku prodejní objednávky.   
    - Pokud aktualizujete některé z těchto data na řádku nákupní objednávky nebo na řádku prodejní objednávky, data na odpovídající objednávce budou automaticky aktualizována.     
    - Nákupní objednávka, která je nastavena na dodávku zboží přímo odběrateli, je propojena s původní prodejní objednávkou prostřednictvím zvláštního přidružení. Toto přidružení ukládá pravidlo, že aktualizace dodacího listu prodejní objednávky nelze provést ze samotné prodejní objednávky a je zapotřebí ji udělat pomocí nákupní objednávky. Avšak fakturace odběratele musí být provedena z prodejní objednávky.  
15. V podokně akcí klikněte na možnost **Zakoupit**.
16. Vyberte **Potvrzení**.
17. Vyberte **OK**.
18. V podokně akcí klikněte na možnost **Přijmout**.
19. Vyberte **Příjemka produktu**.
20. Zadejte hodnotu do pole **Příjemka produktu**.
21. Vyberte **OK**.
22. V podokně akcí klikněte na možnost **Obecné**.
23. Vyberte **Související objednávky** a zvýrazněte požadovaný záznam.
    - Poté, co byla nákupní objednávka aktualizována jako přijatá, nebo jinými slovy, poté, co dodavatel dodal zboží na adresu odběratele, stav původní prodejní objednávky se automaticky aktualizuje na dodáno.  
    - Prodejní objednávku lze nyní vyfakturovat.    
24. Vyberte **OK**.
25. Zavřete stránku.
26. Vyberte **OK**. Zavřete stránky a vraťte se na domovskou stránku.

## <a name="create-direct-deliveries-from-the-workbench"></a>Vytvoření přímé dodávky z pracovní plochy
1. Přejděte na **Navigace > Moduly > Pohledávky > Objednávky > Všechny prodejní objednávky**.
2. Zvolte **Nové**.
3. Zadejte nebo vyberte hodnotu v poli **Účet odběratele** a pak vyberte **OK**.
4. Zadejte nebo vyberte hodnotu v polích **Číslo položky** and **pracoviště**.
5. Rozbalte sekci **Podrobnosti řádku** a vyberte kartu **Dodávka**. Místo vytvoření přímé dodávky v rámci prodejních objednávek jako v předchozím postupu můžete zvolit předání tohoto úkolu nákupčímu. Aby bylo možné zahrnout řádek prodejní objednávky do procesu přímého zpracování, je řádek třeba označit pro přímé dodání.  
6. V poli **Přímá dodávka** vyberte hodnotu **Ano**.
    - Pokud zboží je již výchozím nastavení nastaveno pro přímé dodání, při zadání řádku objednávky bude pole automaticky nastaveno na Ano. Můžete nastavit zboží pro přímou dodávku na základní vydaný produkt nastavením možnosti přímé dodávky na hodnotu Ano a výběrem výchozího skladu přímého dodání.  
    - Protože dosud nebyla vytvořena nákupní objednávka, stav přímé dodávky je nastaven „Pro přímé dodání“.   
7. Zvolte **Uložit**.
8. Zavřete stránky, dokud se nevrátíte na domovskou stránku.
9. Do vyhledávacího panelu zadejte `Direct delivery`.
    - Stránka přímé dodávky se chová jako pracovní plocha pro nákupčí, který poskytuje přehled všech řádků prodejních objednávek, které mají být v přímo doručeny a umožňuje vytvořit odpovídající nákupní objednávky. Kromě toho mohou zobrazit otevření přímé dodávky a potvrzené objednávky na kartě potvrzení a dodání.  
    - Po vytvoření objednávky přímé dodávky se automaticky přesune na kartu Potvrzení. Můžete si vybrat potvrzení objednávky přímo z této stránky. Když je nákup potvrzen, bude automaticky přesunut na kartu dodání, odkud můžete zaregistrovat jeho přijetí.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]