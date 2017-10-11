---
title: "Nastavení externího katalogu pro funkci PunchOut eProcurement"
description: "Toto téma popisuje použití externího katalogu nebo katalogu funkce punchout ke shromažďování informací o nabídce od dodavatele a jejich přidání do žádanky."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4c89f6f168825f7767b836be09fa73b8659b00c6
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="set-up-an-external-catalog-for-punchout-eprocurement"></a>Nastavení externího katalogu pro funkci PunchOut eProcurement

Pomocí externího katalogu můžete zajistit, že informace o produktu a cenách, které následně zpracováváte v aplikaci Dynamics 365 for Finance and Operations, Enterprise edition z července 2017 jsou přesné a aktuální. Žádanku poté lze schválit a převést na nákupní objednávku a tuto objednávku následně zadat u dodavatele.

Když při nastavování externího katalogu zaměstnanec připravuje žádanku, bude mít možnost přesměrovat ji na externí web, do externího katalogu a vrátit košík, který byl vytvořen na externím webu. Tato komunikace vychází z protokolu cXML a je nutné ji nastavit mezi systémy nákupní a prodejní organizace.

Při nastavování komunikace vám musí dodavatel poskytnout informace, které použijete při konfiguraci externího katalogu, jako je identita, doména společnosti kupujících, například DUNS a Číslo DUNS, pověření a adresa URL pro dosažení katalogu dodavatelů.

## <a name="setting-up-an-external-catalog"></a>Nastavení externího katalogu

Externí katalog by měl zaměstnanci, který zadá nákupní žádanku, umožnit přesměrování na externí web pro výběr produktů. Produkty, které zaměstnanec vybere z externího katalogu, jsou vráceny do aplikace Dynamics 365 for Finance and Operations s aktuálními informacemi o ceně a odsud je lze předat do nákupní žádanky. Záměrem je nedovolit zaměstnancům zadat objednávku na externí server. Při nastavování externího katalogu se musíte ujistit, že účel pracoviště, k němuž má přístup externí katalog, je shromažďování informací o nabídce a ne zadání skutečné objednávky.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>K nastavení externího katalogu dodavatelů je třeba dokončit následující úlohy:

1. Nastavte hierarchii kategorií zásobování. Další informace o tom, jak nastavit hierarchii kategorií zásobování, najdete v tématu [Nastavení zásad pro hierarchie kategorie nákupu](/dynamics365/unified-operations/supply-chain/procurement/tasks/set-up-policies-procurement-category-hierarchies).
2. Zaregistrujte dodavatele v modulu Finance and Operations. Dříve, než budete moci nastavit konfigurace pro přístup k externímu katalogu dodavatele, musíte nastavit dodavatele a kontakty dodavatele v aplikaci Microsoft Dynamics 365. Navíc musí být dodavatel externího katalogu přidán do vybrané kategorie zásobování. Další informace o registraci dodavatelů v aplikaci Microsoft Dynamics 365 naleznete v tématu [Správa uživatelů pro spolupráci dodavatele](manage-vendor-collaboration-users.md). Informace o postupu při přidělování dodavatelů ke kategorii zásobování získáte v tématu [Schválení dodavatelů pro konkrétní kategorie zásobování](/dynamics365/unified-operations/supply-chain/procurement/tasks/approve-vendors-specific-procurement-categories).
3. Musí být nastavené měrné jednotky a měna používané dodavatelem. Pro informaci, jak vytvořit měrnou jednotku, přejděte na [Správa měrných jednotek](/dynamics365/unified-operations/supply-chain/pim/tasks/manage-unit-measure).
4. Nakonfigurujte katalog externích dodavatelů na základě požadavků webu katalogu externích dodavatelů. Další informace o této úloze naleznete v další části.
5. Otestujte konfigurace katalogu externích dodavatelů k ověření, že nastavení jsou platná a máte přístup k externímu katalogu dodavatele. Pomocí akce **Ověřit nastavení** ověřte zprávu o nastavení požadavku, kterou jste definovali. Tato zpráva by měla zajistit, že se web externího katalogu otevře v novém okně prohlížeče. Při ověřování nelze objednávat položky a služby od dodavatele. Chcete-li objednat položky a služby, je nutné přejít ke katalogu dodavatele z nákupní žádanky.
6. Aktivujte externí katalog tlačítkem **Aktivovat katalog** na stránce **Externí katalogy**. Externí katalog musí být aktivován před tím, než ho můžou používat zaměstnanci. Externí katalog lze kdykoli deaktivovat.


## <a name="4-configure-the-external-vendor-catalog"></a>(4) konfigurace katalogu externího dodavatele

Tento oddíl uvádí další podrobnosti o úkolu 4 v předchozím oddílu.

1. Zadejte název a popis katalogu externího dodavatele. Název, který zadáte, se zobrazí v nákupním košíku představujícím externí katalog zobrazený zaměstnancům, kteří vytvoří žádanku. Zaměstnanci můžou kliknout na nákupní košík k otevření katalogu na webu externího katalogu dodavatele.
2. Přidejte obrázek pomocí akce **Obrázek externího katalogu**. Obrázek, který zadáte, se zobrazí v nákupním košíku představujícím externí katalog zobrazený zaměstnancům, kteří vytvoří žádanku. Všimněte si, že šířka a výška obrázku musí být stejné. V opačném případě se obrázek nezobrazí správně.
3. Vyberte, zda se má web externího katalogu dodavatele zobrazit ve stejném okně prohlížeče jako web, kde zaměstnanec vytvořil žádanku, nebo v novém okně.
4. Vyberte dodavatele pro katalog. V seznamu **právnické osoby** existuje řádek pro každou právnickou osobu, kde je dodavatel nastaven. Pokud chcete uživatelům umožnit, aby požadovali produkty přímo z katalogu dodavatele v některých právnických osobách, ale ne v jiných, můžete použít tlačítko **Nepovolit přístup** nebo **Povolit přístup** pro každou právnickou osobu, které chcete tento katalog zpřístupnit nebo zamezit v přístupu.
5. V poli **Výchozí konec platnosti (dny)** zadejte počet dní, po které je nabídka přijatá z externího katalogu platná a lze ji použít k nákupu od externího dodavatele. Když je nabídka vytvořena a načtena z místa katalogu externího dodavatele, nabídka je platná od aktuálního systémového data a zůstává v platnosti pro počet dnů, které zadáte v tomto poli.
6. Kliknutím na tlačítko **Přidat** spusťte mapování kategorií zásobování na externí katalog. Potom v seznamu Název kategorie vyberte kategorii. Seznam kategorií je nadřazený kategoriím zásobování, na které je dodavatel namapován ve všech právnických osobách, které jsou nastaveny pro dodavatele.
[!NOTE]
Zásady nákupu slouží k povolení nebo zakázání přístupu ke kategoriím kupující právnické osoby nebo přijímající provozní jednotky. Funkce punchout pro externí katalog vyžaduje, aby přístup být povolen alespoň jedné kategorii zásobování, která je mapována na katalog.
7. Nastavení zprávy s požadavkem cXML, který bude odeslán dodavateli. Automaticky generovaný formát zprávy je minimální šablona potřebné k zahájení relace. Vyplňte hodnoty štítků.

Vždy můžete znovu načíst šablonu zprávy generované systémem klepnutím na **Obnovit formát zprávy**. Všimněte si, že když obnovíte formát zpráv, aktuální zpráva bude nahrazena automaticky generovaným formátem zprávy, který má prázdné značky.

### <a name="cxml-setup-message"></a>Zpráva nastavení cXML
Níže naleznete popis štítků, které jsou zahrnuty do šablony:

| Pole | popis | 
|---------|---------|
|< Záhlaví >< Od >< doména pověření = "" >|Doména společnosti odběratele.|
|< Záhlaví >< Od >< Pověření>< Identita >< /Identita > | Identita společnosti odběratele.|
|< Záhlaví >< Komu >< Doména pověření = "" > | Doména společnosti dodavatele.|
|< Záhlaví >< Komu >< Pověření>< Identita >< /Identita> | Identita společnosti dodavatele.|
|< Záhlaví >< Odesílatel >< Doména pověření=”” > | Doména společnosti odběratele.|
|< Záhlaví >< Odesílatel >< Pověření>< Identita >< /Identita > | Identita společnosti odběratele.|
|< Záhlaví >< Odesílatel >< Pověření >< SharedSecret >< /SharedSecret >|Tajný pro společnost odběratele.|
|< Požadovat deploymentMode=”” >|Testovací nebo výrobní nasazení.|
|< Požadavek >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|Adresa URL konečného bodu punchout společnosti dodavatele.|

### <a name="extrinsic-elements"></a>Externí prvky

Externí prvek představuje další informace jako uživatelské jméno uživatele, který provedl punchout. Je nastaven, když je provedena funkce punchout a může být zaslán ve zprávě o nastavení požadavku.
Dodavatel může mít požadavek na příjem z vnějšího zdroje prvku v nastavení požadavku. V takovém případě byste měli přidat externí prvek do seznamu externích prvků v části **Formát zprávy** na stránce **Externí katalog**. Zadejte název pro externí prvek, který dodavatel rozpozná, a namapujte ho na hodnotu. Možnosti hodnot jsou: uživatelského jméno, uživatelský e-mail nebo náhodná hodnota.
Další informace o protokolu cXML protokolu naleznete na stránkách: http://cxml.org/

## <a name="post-back-message"></a>Zpráva zaslaná zpět
Zpráva zaslaná zpět je zpráva přijatá od dodavatele v případě, že se uživatel odhlásí z externího webu a vrátí do aplikace Finance and Operations. Tyto zprávy nelze konfigurovat. Jsou založeny na definici cXML protokolu. Dále jsou uvedeny informace, které mohou být součástí takové zprávy přijaté na řádku žádanky:

| Zpráva přijatá od dodavatele | Zkopírovaná do řádku žádanky v aplikaci Finance and Operations.|
|------------------------------|----------------------------------------------------------|
|<Množství ItemIn =”” > |Množství|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|ID externí položky|
|< ItemDetail>< UnitPrice >< Měna=”” >| Měna|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Jedn. cena|
|< ItemDetail >< Description ShortName=”” >|Název produktu|
|< ItemDetail >< Description >< /Description >|Zahrnuto v popisu položky, Název produktu, pokud není uveden ShortName.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Jednotka|
|< ItemDetail >< Classification >< /Classification >|Součást popisu položky|
|< ItemDetail >< klasifikace domény = "" >|Součást popisu položky|

## <a name="delete-an-external-catalog"></a>Odstranit externí katalog
Odstraňte externí katalog s akcí odstranění na stránce.

Pokud byl požadován produkt z externího katalogu dodavatele, nelze katalog odstranit, protože uživatel požaduje zboží či službu z tohoto katalogu. Místo toho se stav dodavatel externího katalogu nastaví na neaktivní. Pokud chcete odebrat přístup k webu externího dodavatele katalogu, ale ne ho odstranit, změňte stav externího katalogu na Neaktivní.

