--- 
title: "Expedování objednávek jako přímých dodávek"
description: "Tento postup ukazuje, jak vytvořit přímé dodávky pro prodejní objednávku."
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d98e288a157183fbf4d7c032d86bb4a65166e297
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="ship-orders-as-direct-deliveries"></a>Expedování objednávek jako přímých dodávek

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje, jak vytvořit přímé dodávky pro prodejní objednávku. Přímou dodávku používejte, pokud chcete zboží expedovat odběrateli přímo od dodavatele, místo expedice nejprve do svého vlastního skladu,. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. K úspěšnému dokončení druhého podúkolu „Vytvoření přímé dodávky z pracovní plochy“ se ujistěte, že zboží, která vyberete v prodejní objednávce, má určeného výchozího dodavatele na pevné kartě Nákup vydaného základního produktu.


## <a name="set-an-individual-order-for-direct-delivery"></a>Nastavení jednotlivé objednávky pro přímé dodání
1. Přejděte na Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele zadejte nebo vyberte hodnotu.
    * Pokud používáte data USMF, můžete vybrat účet US-001.  
4. Klikněte na tlačítko OK.
5. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Pokud používáte data USMF, můžete vybrat položku T0020.  
6. Klikněte na položku Uložit.
7. V podokně akcí klikněte na položku Prodejní objednávka.
8. Klikněte na položku Přímá dodávka.
    * Vytvoření seznamů stránek dodávek všech otevřených řádků prodejních objednávek jako kopírovaných z prodejní objednávky. Můžete zkontrolovat podrobnosti o objednávce, a v případě potřeby můžete upravit podrobnosti jako například nákupní množství a podmínek cen předtím, než vytvoříte přímou dodávku.  
9. V poli Zahrnout vše vyberte možnost Ano.
    * Pokud chcete generovat přímou dodávku pouze pro podmnožinu řádků prodejních objednávek, vyberte je jednotlivě.  
    * Pole účtu dodavatele může nebo nemusí být vyplněno číslem dodavatele. Pokud bude výchozí dodavatele nastaven pro produkt (v přidružené disponibilitě položky), pak do řádku bude zkopírován tento dodavatel. V ostatních případech musíte dodavatele zadat ručně. V tomto příkladu vybereme nového dodavatele v dalším kroku i v případě, že jeden je již vyplněn.   
10. V poli Účet dodavatele zadejte nebo vyberte hodnotu.
    * Pokud používáte data USMF, můžete vybrat účet 1001.  
11. Klikněte na tlačítko OK.
    * Zpráva vás informuje o tom, že nákupní objednávka nyní byla vytvořena.   
12. Rozbalte sekci Podrobnosti řádku.
13. Klikněte na záložku Dodání.
    * Pole Přímá dodávka je nyní nastaveno na hodnotu Ano.  
    * Stav přímé dodávky zobrazuje vytvořenou nákupní objednávku.   
14. V podokně akcí klikněte na položku Obecné.
15. Klepněte na Související objednávky.
16. Kliknutím přejdete na odkaz v poli Nákupní objednávka.
17. Rozbalte sekci Podrobnosti řádku.
18. Klepněte na kartu Adresa.
    * Všimněte si, že doručovací adresa pro tento řádek nákupní objednávky je adresa dodání odběratele, a nikoli adresa vaší společnosti.  
    * Pokud upravíte adresu dodání na řádku prodejní objednávky nebo na řádku původní nákupní objednávky, bude adresa automaticky aktualizována na řádku odpovídající objednávky.  
19. Klikněte na záložku Dodání.
    * Stejně jako řádek prodejní objednávky je typ řádku přidružené nákupní objednávky také nastaven na přímou dodávku.  
    * Datum dodání na řádku nákupní objednávky a potvrzené datum dodání jsou v uvedeném pořadí nastaveny k požadovanému datu příjmu a potvrzenému datu příjmu původního řádku prodejní objednávky.   
    * Pokud aktualizujete některé z těchto data na řádku nákupní objednávky nebo na řádku prodejní objednávky, data na odpovídající objednávce budou automaticky aktualizována.     
    * Nákupní objednávka, která je nastavena na dodávku zboží přímo odběrateli, je propojena s původní prodejní objednávkou prostřednictvím zvláštního přidružení. Toto přidružení ukládá pravidlo, že aktualizace dodacího listu prodejní objednávky nelze provést ze samotné prodejní objednávky a je zapotřebí ji udělat pomocí nákupní objednávky. Avšak fakturace odběratele musí být provedena z prodejní objednávky.  
20. V podokně akcí klikněte na položku Nákup.
21. Klikněte na možnost Potvrzení.
22. Klikněte na tlačítko OK.
23. V podokně akcí klikněte na položku Přijmout.
24. Klikněte na položku Příjemka produktu.
25. Zadejte hodnotu do pole Příjemka produktu.
26. Klikněte na tlačítko OK.
27. V podokně akcí klikněte na položku Obecné.
28. Klepněte na Související objednávky.
29. Označte v seznamu vybraný řádek.
    * Poté, co byla nákupní objednávka aktualizována jako přijatá, nebo jinými slovy, poté, co dodavatel dodal zboží na adresu odběratele, stav původní prodejní objednávky se automaticky aktualizuje na dodáno.  
    * Prodejní objednávku lze nyní vyfakturovat.    
30. Klikněte na tlačítko OK.
31. Zavřete stránku.
32. Klikněte na tlačítko OK.

## <a name="create-direct-deliveries-from-the-workbench"></a>Vytvoření přímé dodávky z pracovní plochy
1. Zavřete stránku.
2. Zavřete stránku.
3. Přejděte na Všechny prodejní objednávky.
4. Klikněte na položku Nová.
5. V poli Účet odběratele zadejte nebo vyberte hodnotu.
6. Klepněte na tlačítko OK.
7. V poli Číslo zboží zadejte nebo vyberte hodnotu.
8. Rozbalte sekci Podrobnosti řádku.
9. Klikněte na záložku Dodání.
    * Místo vytvoření přímé dodávky v rámci prodejních objednávek jako v předchozím postupu můžete zvolit předání tohoto úkolu nákupčímu. Aby bylo možné zahrnout řádek prodejní objednávky do procesu přímého zpracování, je řádek třeba označit pro přímé dodání.  
10. V poli Přímá dodávka vyberte hodnotu Ano.
    *   Pokud zboží je již výchozím nastavení nastaveno pro přímé dodání, při zadání řádku objednávky bude pole automaticky nastaveno na Ano. Můžete nastavit zboží pro přímou dodávku na základní vydaný produkt nastavením možnosti přímé dodávky na hodnotu Ano a výběrem výchozího skladu přímého dodání.  
    * Protože dosud nebyla vytvořena nákupní objednávka, stav přímé dodávky je nastaven pro přímé dodání.   
11. Zavřete stránku.
12. Zavřete stránku.
13. Přejděte na Přímá dodávka.
    * Stránka přímé dodávky se chová jako pracovní plocha pro nákupčí, který poskytuje přehled všech řádků prodejních objednávek, které mají být v přímo doručeny a umožňuje vytvořit odpovídající nákupní objednávky. Kromě toho mohou zobrazit otevření přímé dodávky a potvrzené objednávky na kartě potvrzení a dodání.   
14. Klepněte na Vytvořit objednávku s přímým dodáním.
15. Klepněte na kartu Potvrzení.
    * Po vytvoření objednávky přímé dodávky, se automaticky přesune na kartu potvrzení. Můžete potvrdit objednávku přímo z této stránky. Když je nákup potvrzen, bude automaticky přesunut na kartu dodání, odkud můžete zaregistrovat jeho přijetí.  


