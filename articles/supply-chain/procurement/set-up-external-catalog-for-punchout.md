---
title: Nastavení externího katalogu pro funkci PunchOut eProcurement
description: Toto téma popisuje použití externího katalogu nebo katalogu funkce PunchOut ke shromažďování informací o nabídce od dodavatele a jejich přidání do žádanky.
author: RichardLuan
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchVendorPortalRequests, CatExternalCatalogConfiguration, CatCXMLCartLogList
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa383e7e026e379c8016d9c160ccc8b1405392ad
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237342"
---
# <a name="set-up-an-external-catalog-for-punchout-e-procurement"></a>Nastavení externího katalogu pro funkci PunchOut eProcurement

[!include [banner](../includes/banner.md)]

Pomocí externího katalogu můžete zajistit, zda jsou informace o produktu a cenách, které následně zpracováváte v aplikaci Supply Chain Management, přesné a aktuální. Žádanku poté lze schválit a převést na nákupní objednávku a tuto objednávku následně zadat u dodavatele.

Když při nastavování externího katalogu zaměstnanec připravuje žádanku, bude mít možnost přesměrovat ji na externí web, do externího katalogu a vrátit košík, který byl vytvořen na externím webu. Tato komunikace vychází z protokolu cXML a je nutné ji nastavit mezi systémy nákupní a prodejní organizace.

Při nastavování komunikace vám musí dodavatel poskytnout informace, které použijete při konfiguraci externího katalogu, jako je identita, doména společnosti kupujících, například DUNS a Číslo DUNS, pověření a adresa URL pro dosažení katalogu dodavatelů.

## <a name="setting-up-an-external-catalog"></a>Nastavení externího katalogu

Externí katalog by měl zaměstnanci, který zadá nákupní žádanku, umožnit přesměrování na externí web pro výběr produktů. Produkty, které zaměstnanec vybere z externího katalogu, jsou vráceny s aktuálními informacemi o ceně a odsud je lze předat do nákupní žádanky. Záměrem je nedovolit zaměstnancům zadat objednávku na externí server. Při nastavování externího katalogu se musíte ujistit, že účel pracoviště, k němuž má přístup externí katalog, je shromažďování informací o nabídce a ne zadání skutečné objednávky.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>K nastavení externího katalogu dodavatelů je třeba dokončit následující úlohy:

1. Nastavte hierarchii kategorií zásobování. Další informace o tom, jak nastavit hierarchii kategorií zásobování, najdete v tématu [Nastavení zásad pro hierarchie kategorie nákupu](tasks/set-up-policies-procurement-category-hierarchies.md).
2. Zaregistrujte dodavatele v aplikaci Supply Chain Management. Dříve, než budete moci nastavit konfigurace pro přístup k externímu katalogu dodavatele, musíte nastavit dodavatele a kontakty dodavatele v aplikaci Microsoft Dynamics 365. Navíc musí být dodavatel externího katalogu přidán do vybrané kategorie zásobování. Další informace o registraci dodavatelů naleznete v tématu [Správa uživatelů pro spolupráci dodavatele](manage-vendor-collaboration-users.md). Informace o postupu při přidělování dodavatelů ke kategorii zásobování získáte v tématu [Schválení dodavatelů pro konkrétní kategorie zásobování](tasks/approve-vendors-specific-procurement-categories.md).
3. Musí být nastavené měrné jednotky a měna používané dodavatelem. Pro informaci, jak vytvořit měrnou jednotku, přejděte na [Správa měrné jednotky](../pim/tasks/manage-unit-measure.md).
4. Nakonfigurujte katalog externích dodavatelů na základě požadavků webu katalogu externích dodavatelů. Další informace o této úloze naleznete v části [Konfigurace katalogu externího dodavatele](#configure-the-external-vendor-catalog).
5. Otestujte konfigurace katalogu externích dodavatelů k ověření, že nastavení jsou platná a máte přístup k externímu katalogu dodavatele. Pomocí akce **Ověřit nastavení** ověřte zprávu o nastavení požadavku, kterou jste definovali. Tato zpráva by měla zajistit, že se web externího katalogu otevře v novém okně prohlížeče. Při ověřování nelze objednávat položky a služby od dodavatele. Chcete-li objednat položky a služby, je nutné přejít ke katalogu dodavatele z nákupní žádanky.
6. Aktivujte externí katalog tlačítkem **Aktivovat katalog** na stránce **Externí katalogy**. Externí katalog musí být aktivován před tím, než ho můžou používat zaměstnanci. Externí katalog lze kdykoli deaktivovat.


## <a name="configure-the-external-vendor-catalog"></a>Konfigurace katalogu externího dodavatele

Tento oddíl uvádí další podrobnosti o úkolu 4 v předchozím oddílu.

1. Zadejte název a popis katalogu externího dodavatele. Název, který zadáte, se zobrazí v nákupním košíku představujícím externí katalog zobrazený zaměstnancům, kteří vytvoří žádanku. Zaměstnanci můžou kliknout na nákupní košík k otevření katalogu na webu externího katalogu dodavatele.
2. Přidejte obrázek pomocí akce **Obrázek externího katalogu**. Obrázek, který zadáte, se zobrazí v nákupním košíku představujícím externí katalog zobrazený zaměstnancům, kteří vytvoří žádanku. Všimněte si, že šířka a výška obrázku musí být stejné. V opačném případě se obrázek nezobrazí správně.
3. Vyberte, zda se má web externího katalogu dodavatele zobrazit ve stejném okně prohlížeče jako web, kde zaměstnanec vytvořil žádanku, nebo v novém okně.
4. Vyberte dodavatele pro katalog. V seznamu **právnické osoby** existuje řádek pro každou právnickou osobu, kde je dodavatel nastaven. Pokud chcete uživatelům umožnit, aby požadovali produkty přímo z katalogu dodavatele v některých právnických osobách, ale ne v jiných, můžete použít tlačítko **Nepovolit přístup** nebo **Povolit přístup** pro každou právnickou osobu, které chcete tento katalog zpřístupnit nebo zamezit v přístupu.
5. V poli **Výchozí konec platnosti (dny)** zadejte počet dní, po které je nabídka přijatá z externího katalogu platná a lze ji použít k nákupu od externího dodavatele. Když je nabídka vytvořena a načtena z místa katalogu externího dodavatele, nabídka je platná od aktuálního systémového data a zůstává v platnosti pro počet dnů, které zadáte v tomto poli.
6. Kliknutím na tlačítko **Přidat** spusťte mapování kategorií zásobování na externí katalog. Potom v seznamu Název kategorie vyberte kategorii. Seznam kategorií je nadřazený kategoriím zásobování, na které je dodavatel namapován ve všech právnických osobách, které jsou nastaveny pro dodavatele.

    > [!NOTE]
    > Zásady nákupu slouží k povolení nebo zakázání přístupu ke kategoriím kupující právnické osoby nebo přijímající provozní jednotky. Funkce punchout pro externí katalog vyžaduje, aby přístup být povolen alespoň jedné kategorii zásobování, která je mapována na katalog.

7. Nastavení zprávy s požadavkem cXML, který bude odeslán dodavateli. Automaticky generovaný formát zprávy je minimální šablona potřebné k zahájení relace. Vyplňte hodnoty štítků.

Vždy můžete znovu načíst šablonu zprávy generované systémem klepnutím na **Obnovit formát zprávy**. Všimněte si, že když obnovíte formát zpráv, aktuální zpráva bude nahrazena automaticky generovaným formátem zprávy, který má prázdné značky.

### <a name="cxml-setup-message"></a>Zpráva nastavení cXML
Níže naleznete popis štítků, které jsou zahrnuty do šablony:

| Pole | popis | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|Doména společnosti odběratele.|
|< Header >< From >< Credential>< Identity >< /Identity > | Identita společnosti odběratele.|
|< Header >< To >< Credential domain=”” > | Doména společnosti dodavatele.|
|< Header >< To >< Credential>< Identity >< /Identity> | Identita společnosti dodavatele.|
|< Header >< Sender >< Credential domain=”” > | Doména společnosti odběratele.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | Identita společnosti odběratele.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|Tajný pro společnost odběratele.|
|< Request deploymentMode=”” >|Testovací nebo výrobní nasazení.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|Adresa URL konečného bodu PunchOut společnosti dodavatele.|

### <a name="extrinsic-elements"></a>Externí prvky

Externí prvek představuje další informace jako uživatelské jméno uživatele, který provedl punchout. Je nastaven, když je provedena funkce PunchOut a může být zaslán ve zprávě o nastavení požadavku.
Dodavatel může mít požadavek na příjem z vnějšího zdroje prvku v nastavení požadavku. V takovém případě byste měli přidat externí prvek do seznamu externích prvků v části **Formát zprávy** na stránce **Externí katalog**.
Zadejte název pro externí prvek, který dodavatel rozpozná, a namapujte ho na hodnotu. Možnosti hodnot jsou: uživatelského jméno, uživatelský e-mail nebo náhodná hodnota.
Další informace o protokolu cXML protokolu naleznete na webu [cXML.org](http://cxml.org/).

## <a name="post-back-message"></a>Zpráva zaslaná zpět
Zpráva zaslaná zpět je zpráva přijatá od dodavatele v případě, že se uživatel odhlásí z externího webu a vrátí do aplikace Supply Chain Management. Tyto zprávy nelze konfigurovat. Jsou založeny na definici cXML protokolu. Dále jsou uvedeny informace, které mohou být součástí takové zprávy přijaté na řádku žádanky.

| Zpráva přijatá od dodavatele | Zkopírováno do řádku žádanky|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Množství|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|ID externí položky|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Měna|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Jedn. cena|
|< ItemDetail >< Description ShortName=”” >|Název produktu|
|< ItemDetail >< Description >< /Description >|Zahrnuto v popisu položky, Název produktu, pokud není uveden ShortName.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Jednotka|
|< ItemDetail >< Classification >< /Classification >|Součást popisu položky|
|< ItemDetail >< Classification domain=”” >|Součást popisu položky|

## <a name="delete-an-external-catalog"></a>Odstranit externí katalog
Odstraňte externí katalog s akcí odstranění na stránce.

Pokud byl požadován produkt z externího katalogu dodavatele, nelze katalog odstranit, protože uživatel požaduje zboží či službu z tohoto katalogu. Místo toho se stav dodavatel externího katalogu nastaví na neaktivní. Pokud chcete odebrat přístup k webu externího dodavatele katalogu, ale ne ho odstranit, změňte stav externího katalogu na Neaktivní.

## <a name="additional-resources"></a>Další prostředky

- [cXML vylepšení nákupu](purchasing-cxml-enhancements.md)
- [Použití externích katalogů pro funkci PunchOut eProcurement](use-external-catalogs-for-punchout.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]