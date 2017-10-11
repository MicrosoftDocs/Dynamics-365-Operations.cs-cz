---
title: "Příjem produktů proti nákupním objednávkám"
description: "Tento článek popisuje různé možnosti pro registraci produktů jako přijatých."
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 93113
ms.assetid: d4ec3e86-fce2-4546-911b-e0acf64c8887
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a192688315adb2d83f349c525c5d8f70309375db
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="product-receipt-against-purchase-orders"></a>Příjem produktů proti nákupním objednávkám

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Tento článek popisuje různé možnosti pro registraci produktů jako přijatých.

Příjemka produktu je procesem zaznamenávání toho, že výrobky, které byly objednány, byly přijaty, a řádky nákupní objednávky tak mohou být zpracovány pro fakturaci. V některých případech produkty procházejí předběžnou registrací, kde jsou zaznamenány další informace od dodavatele před přijetím produktů. Po příchodu produktů jsou nejprve označeny jako **Registrované**. Produkty pak mohou projít dalším zpracováním, jako je řízení kvality, než budou nakonec označeny jako **Přijato**.

## <a name="preregistration-asn"></a>Předběžná registrace (ASN)
Dodavatelé mohou sdílet informace o produktech, které budou dodány. V tomto případě lze předregistrovat produkty a zaznamenat tyto informace dříve, než budou produkty přijaty. Předregistrací produktů můžete snížit množství práce vyžadované během registrace a příjmu položek. Dodavatelé mohou poskytovat informace o produktech elektronicky prostřednictvím avíza expedice zboží, které je poté automaticky zaznamenané do systému. Informace v avízu expedice zboží zahrnují množství produktů, které budou dodány, a datum, kdy budou dodány. Avízo expedice zboží může také obsahovat informace, jako například informace o dávce a sériovém číslu. Registrace avíza expedice zboží probíhá v modulu **Správa přepravy**.

## <a name="registration"></a>Registrace
K registraci příjmu produktu často dochází na vstupním přepravišti ve skladu. Provádí se buď pomocí kapesních zařízení, nebo prostřednictvím deníků doručení. Případně můžete ručně zaregistrovat příjemky produktu pomocí akce **Registrace** na stránce **Nákupní objednávky**. V obou případech jsou výrobky označeny jako **Registrované**. Všimněte si, že produkty nejsou dosud označeny jako **Přijato**.  

Produkty, které jsou přijaty ve skladu, mohou projít kontrolu kvality předtím, než dojde k jejich zaskladnění do zásob. Při kontrole kvality lze použít jak objednávky kvality, tak karanténní příkazy. Pokud jsou použity objednávky kvality, můžete nakonfigurovat proces tak, že dojde k dočasnému zablokování produktů skrze rezervaci, zatímco bude probíhat jejich inspekce. Pokud jsou použity karanténní příkazy, produkty jsou přesunuty do jiného skladu pro kontrolu. Tento sklad je označován jako karanténní sklad. V obou procesech kontroly kvality může být některé zboží vyřazeno, protože neodpovídá očekávané kvalitě, nebo protože kontrola kvality zahrnuje destruktivní testování vzorku výrobku.

## <a name="product-receipt"></a>Příjemka produktu
Nejčastěji se používá akce **Příjemka produktu** na stránce **Nákupní objednávky** k označení produktů jako **Přijato** v nákupní objednávce. Stránka **Zaúčtování příjemky produktu** má různé možnosti pro množství, které je zaúčtováno jako přijaté. Například můžete nastavit pole **Množství** na **Objednané množství** nebo **Množství nynějšího příjmu**. Případně pokud byl použit proces příjezdu do skladu, často se toto pole nastaví na hodnotu **Registrované množství**. Můžete upravit množství na každém řádku objednávky, který bude označen jako **Přijato**, a zohlednit tak případné nesrovnalosti, jako je nadměrná/nedostatečná dodávka. Během příjmu produktu je nutné zadat identifikátor příjemky produktu, což je obvykle odkaz na dodací list od dodavatele. Tento identifikátor je vyžadován pro účetnictví, protože umožňuje kontrolu a audity dodacích listů dodavatel proti přijatému zboží a zaúčtovaným zásobám nebo nákladům.  

Pokud zaměstnanec objednal zboží pomocí nákupní žádanky, tento zaměstnanec může být vyzván, aby přijetí produktu sám potvrdil. Můžete konfigurovat toto chování pomocí pracovního postupu. Podmínky pracovního postupu můžete nakonfigurovat tak, aby odpovídaly vašemu obchodnímu procesu.  

Nákupní objednávky lze vytvářet pro produkty, které nejsou určeny jako zásoby, ale jsou považovány za výdaje. Tato kategorie obsahuje řádky objednávky, kde jsou výrobky označeny jako **Není na skladě** podle jejich skupiny skladového modelu, a také řádků, které používají kategorie zásobování. V tomto případě zboží nemusí procházet registrací doručení a přijetím ve skladu. Místo toho se používá akce **Příjemka produktu** k zaznamenání příjmu přímo v nákupní objednávce, a příjem je založen na objednaném množství, nikoli na zaznamenaném množství.  

Můžete vytvořit řádky nákupní objednávky, kde je povolena možnost **Nový dlouhodobý majetek**. Tato možnost označuje, že nákup by se měl považovat za dlouhodobý majetek namísto zásob. V tomto případě nastavená pravidla určení dlouhodobého majetku stanovují, zda nákup produktu nebo kategorie překračuje určité prahy, a musí proto být zaznamenány jako majetek a projít správu dlouhodobého majetku. Nákup lze provést také směrem k existujícímu dlouhodobému majetku. V tomto případě je částka podle potřeby upravena.  

Můžete vybrat více objednávek a zpracovat příjem u všech těchto objednávek společně. Tento postup není velmi často používány, ale můžete jej použít, pokud má dodavatel vaše dodávky konsolidované do jediného balíčku. Během příjmu produktu u nákupu je vám k dispozici funkce pro provedení souhrnné aktualizace. Souhrnné aktualizace umožňují zaúčtovat jeden dodacího list od dodavatele pro více než jednu nákupní objednávku.  

Nákupní objednávky můžete vytvořit z prodejní objednávky, kde byla vybrána možnost **Přímá dodávka**. Při použití přímé dodávky nejsou produkty nikdy doručeny do skladu, ale jsou dodány přímo od dodavatele k zákazníkovi. V tomto případě je příjem obvykle zaznamenán přímo v nákupní objednávce. Příjem může probíhat automaticky, například pomocí integrace EDI s dodavatelem. Případně pokud je nákupní objednávka mezipodnikovou nákupní objednávkou, aplikace Microsoft Dynamics 365 for Finance and Operations automatizuje příjem v mezipodnikové prodejní objednávce, když dojde k dodávce. Při použití přímého dodání jsou výrobky i nadále zpracovány jako zásoby, i když nejsou fyzicky přijaty ve skladu. Proto při registraci příjemky produktu z nákupní objednávky je prodejní objednávka automaticky aktualizována v dodacím listu tak, aby celkové změny zásob byly 0 (nulové). V případech využívajících přímé doručení byste neměly vyžadovat předběžnou registraci. Pokud používáte sklady, které jsou povoleny pro řízení skladu, můžete obejít požadavek na registraci registrační značky zadáním virtuálního skladu. Tento sklad určíte v poli **Sklad pro přímé dodávky** u produktu. 

Po zpracování příjemky produktu na nákupní objednávce je stav nákupní objednávky nastaven na **Přijato**, což označuje, že lze fakturu zpracovat pro objednávku. Můžete zkontrolovat podrobnosti o produktech, které již byly přijaty, pomocí stránky **Deníky příjemek produktu**.  

Přístup k této stránce je pomocí skupiny akci **Příjem** na stránce **Nákupní objednávka**. Informace v denících zahrnují podrobné informace o množství, datech a rozměrech.

<a name="see-also"></a>Viz také
--------

[Přehled nákupních objednávek](purchase-order-overview.md)

[Vytvoření nákupní objednávky](purchase-order-creation.md)

[Potvrzení a odmítnutí nákupní objednávky](purchase-order-approval-confirmation.md)

[Přehled faktur dodavatele](/dynamics365/unified-operations/financials/accounts-payable/vendor-invoices-overview)



