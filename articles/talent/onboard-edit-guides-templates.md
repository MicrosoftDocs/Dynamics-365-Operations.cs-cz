---
title: Úprava průvodců a šablon zaškolení v aplikaci Dynamics 365 Talent - Onboard
description: V tomto tématu je vysvětleno, jak přidat aktivity a další informace do průvodců a šablon zaškolení v aplikaci Microsoft Dynamics 365 Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460584"
---
# <a name="edit-onboarding-guides-and-templates"></a>Úprava průvodců a šablon zaškolení

[!include [banner](includes/banner.md)]

Po vytvoření průvodce nebo šablony zaškolení v aplikaci Microsoft Dynamics 365 Talent: Onboard je nutné přidat úvod, aktivity, kontakty a zdroje. Onboard umožňuje zahrnout do průvodců zaškolením bohatý obsah včetně následujících možností:

- Videa na YouTube
- Prezentace Microsoft Sway
- Aplikace Microsoft PowerApps
- Videa na Microsoft Stream
- Formuláře Microsoft Forms
- Prvky IFrame, které obsahují webový obsah

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>Úprava úvodů nebo aktivit importovaných ze šablony

Pokud vytvoříte průvodce zaškolením ze šablony nebo pokud importujete aktivity z jedné šablony do druhé, zobrazí se u importovaných aktivit tlačítko **zámku**. Označují se jako *spravované aktivity*.

[![Spravované aktivity](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

Když vyberete spravovanou aktivitu, uvidíte v její horní části zdrojovou šablonu.

[![Zdroj spravované aktivity](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

Když upravíte aktivitu v šabloně, Onboard populuje změny do všech šablon a neodeslaných průvodců založených na dané šabloně. Pokud vyberete neodeslaného průvodce na základě upravené šablony a poté vyberete kartu **Aktivity** v průvodci, zobrazí se upozornění, že se průvodce změnil. Chcete-li oznámení zrušit, vyberte **OK**. 

[![Oznámení o změně](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

Vedle aktualizovaných aktivit se zobrazí černá tečka.

[![Změněná aktivita](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

Spravované aktivity nelze upravovat mimo původní šablonu, s výjimkou přidání nabyvatele, data splatnosti nebo jiných informací do pravé části aktivity.

Chcete-li upravit spravovanou aktivitu nebo nechcete, aby aktivita přijímala aktualizace z šablony, ze které pochází, vyberte pro danou aktivitu tlačítko **zámku**. Tlačítko **zámku** zmizí. Tato aktivita již nebude spravována původní šablonou a nebude již moci získávat aktualizace z této šablony. Aktualizace provedené v aktivitě nemají vliv na původní šablonu.

Odstraníte-li aktivitu z průvodce a provedete změny ze šablony tohoto průvoce, aktivita zůstane v průvodci odstraněná.

> [!NOTE]
> Kontakty a zdroje nejsou spravovány šablonami. Kromě toho nejsou tyto oddíly spravovány, takže pokud přidáte nebo upravíte oddíl v šabloně, změny nebudou vloženy do žádných průvodců nebo šablon, které tuto šablonu používají.
> 
> Přidáte-li do šablony nové aktivity, budou nové aktivity přesunuty do průvodců a šablon na základě této šablony a nové aktivity se zobrazí nahoře.

## <a name="import-activities-from-another-template"></a>Import aktivit z jiné šablony

Do průvoce nebo šablony můžete importovat aktivity z jedné nebo více šablon.

1. Vyberte průvodce nebo šablonu, které chcete upravit.

2. Vyberte karu **Aktivity**.

3. V části vpravo vyberte kartu **Import**.

   [![Aktivity importu](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. Chcete-li zobrazit náhled úkolů na nové kartě v prohlížeči, vyberte tlačítko **Otevřít na nové kartě** v libovolné šabloně.

   [![Import aktivit](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. Požadovanou šablonu přetáhněte na místo v šabloně průvodce, kde se mají zobrazovat aktivity. Pokračujte v úpravách příručky nebo šablony.

Importované aktivity budou obsahovat tlačítko **zámku**, které označuje, že tyto aktivity jsou spravovány šablonou, ze které jste importovali. Po provedení změn importované šablony se tyto aktivity aktualizují v šabloně, do které byly importovány. Změny však nebudou automaticky vloženy do žádných průvodců vytvořených ze šablony, do které jste importovali data.

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>Zadání změn ze šablony do jiných šablon nebo průvodců

Pokud upravíte šablonu, která obsahuje aktivity používané v jiných šablonách nebo průvodcích, musíte tyto změny použít, pokud je chcete zobrazit v jiných šablonách nebo průvodcích.

Pokud si nejste jisti, zda jsou aktivity šablony použity v jiných šablonách nebo průvodcích, vyberte kartu **Použito na** k zobrazení, kde se tyto aktivity zobrazují.

   [![Zobrazení, kde se používají průvodci a šablony](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

Postup použití změn:

1. Uložte změny výběrem tlačítka **Uložit**. Pokud tak neučiníte, budete vyzváni k uložení změn v následujícím kroku.

2. Vyberte **Použít tyto změny**.

   
## <a name="add-or-edit-an-introduction"></a>Přidání nebo úprava úvodu

1. Na kartě **Úvod** zadejte název průvodce a otevřenou zprávu. Chcete-li použít vzorový text, vyberte **Použít tuto zprávu**.

    [![Karta Úvod v šabloně zaškolení](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. Pomocí tlačítek pro formátování můžete vyvolat text podle potřeby nebo přidat obrázky nebo odkazy.
3. Práci uložte výběrem možnosti **Uložit**.

## <a name="add-or-edit-activities"></a>Přidání nebo úprava aktivit

1. Na kartě **Aktivity** přetáhněte položky z pravé části do oblasti pro úpravy.
2. Chcete-li průvodce uspořádat do oddílů, přetáhněte položku **Nový oddíl** do oblasti pro úpravy a zadejte název a volitelný popis oddílu.

    ![[Přidání nové sekce do průvodce zaškolením nebo šablony](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. Chcete-li přidat aktivity pro nově přijatého zaměstnance k dokončení, přetáhněte položku **Nová aktivita** do oblasti pro úpravy a zadejte název a popis aktivity.

    ![[Přidání nové aktivity do průvodce zaškolením nebo šablony](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. Přidání bohatého obsahu do průvodce zaškolením:

    - Chcete-li přidat video YouTube, přetáhněte položku **YouTube** do oblasti pro úpravy, zadejte název a popis aktivity a zadejte adresu URL videa na YouTube.
    - Chcete-li přidat prezentaci Sway nebo zpravodaj, přetáhněte položku **Sway** do oblasti pro úpravy, zadejte název a popis aktivity a zadejte vloženou adresu URL pro prezentaci Sway nebo zpravodaj.
    - Chcete-li přidat aplikaci Microsoft Power Apps, přetáhněte položku **Power Apps** do oblasti pro úpravy, zadejte název a popis aktivity a vyberte aplikaci Power Apps nebo zadejte ID aplikace Power Apps.
    - Chcete-li přidat video Microsoft Stream, přetáhněte položku **Microsoft Stream** do oblasti pro úpravy, zadejte název a popis aktivity a zadejte adresu URL videa na Microsoft Stream.
    - Chcete-li přidat formulář Microsoft Forms, přetáhněte položku **Microsoft Forms** do oblasti pro úpravy, zadejte název a popis aktivity, zadejte adresu URL formuláře Microsoft Forms a určete velikost oblasti obrazovky.
    - Chcete-li přidat iframe obsahující webový obsah, přetáhněte položku **Webový obsah (iframe)** do oblasti pro úpravy, zadejte název a popis aktivity, zadejte adresu URL webového obsahu a určete velikost oblasti obrazovky.

    ![[Přidání bohatého obsahu do průvodce zaškolením nebo šablony](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. Volitelné: v oblasti napravo od každé aktivity přiřaďte tuto aktivitu konkrétní osobě nebo roli, přidejte datum splatnosti a kontaktní osobu a přiřaďte barvu kategorie. Když přiřadíte aktivitu osobě nebo roli, bude úkol vytvořen pro každou jednotlivou osobu. Tento úkol se zobrazí v nabídce **Úkoly** v aplikaci Onboard.

    [![Přiřazení aktivity v průvodci nebo šabloně zaškolení](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. Práci uložte výběrem možnosti **Uložit**.

Chcete-li odstranit aktivitu nebo oddíl, vyberte tlačítko **Odstranit** (symbol odpadkového koše) v pravém horním rohu aktivity nebo oddílu.

Chcete-li změnit pořadí aktivit a oddílů, přetáhněte je do nového umístění.

## <a name="add-or-edit-contacts"></a>Přidání nebo úprava kontaktů

Můžete přidat kontaktní osobu, která může nově přijatému zaměstnanci dosahovat úspěchů od prvního dne. Těmito kontakty mohou být náboroví pracovníci, kolegové z týmu, kamarádi při zaškolení, mentoři, správci a zaměstnanci podpory IT.

1. Na kartě **Kontakty** vyberte možnost **Nový kontakt**.
2. V dialogovém okně **Přidat člena týmu** zadejte jméno nebo e-mailovou adresu kontaktní osoby, zadejte krátký popis, který vysvětluje, jakým způsobem může kontaktní osoba pomoci nově přijatému zaměstnanci a poté vyberte **Přidat**. 

    ![[Přidání kontaktů do průvodce zaškolením nebo šablony](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    Případně můžete vybrat jeden nebo více kontaktů v nabídce **Návrhy.**

3. Práci uložte výběrem možnosti **Uložit**.

Chcete-li odstranit kontakt, vyberte tlačítko **Odstranit** (symbol odpadkového koše) napravo od kontaktu.

Chcete-li upravit kontakt, vyberte tlačítko **Upravit** (symbol pera) napravo od kontaktu.

## <a name="add-or-edit-resources"></a>Přidání nebo úprava zdrojů

V rámci vlastního průvodce zaškolením můžete přidat užitečné soubory, mapy a odkazy do části **Zdroje**.

1. Na kartě **Zdroje** vyberte možnost **Nový zdroj**.
2. Proveďte jeden z následujících kroků:

    - Chcete-li přidat soubor, vyberte kartu **Soubor** a přetáhněte jej do vymezené oblasti. (Případně můžete kliknout na libovolné místo v této oblasti a vyhledat soubor v počítači nebo vybrat možnost **Procházet OneDrive**.) Zadejte název souboru a poté klikněte na tlačítko **Přidat**.
    - Pokud chcete přidat odkaz, vyberte kartu **Odkaz**, zadejte název a adresu odkazu a vyberte **Přidat**.
    - Pokud chcete přidat mapu, vyberte kartu **Mapa**, zadejte název a adresu mapy a vyberte **Přidat**. Onboard bude obsahovat mapu zadané adresy.

    ![[Přidání prostředku do průvodce zaškolením nebo šablony](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. Práci uložte výběrem možnosti **Uložit**.

Chcete-li odstranit zdroj, vyberte tlačítko **Odstranit** (symbol odpadkového koše) napravo od zdroje.

Chcete-li upravit zdroj, vyberte tlačítko **Upravit** (symbol pera) napravo od zdroje.

## <a name="next-steps"></a>Další kroky

- [Sdílení obsahu s jinými přispěvateli](./onboard-share-template.md)
- [Zobrazit stav úkolů a zaškolení zaměstnanců](./onboard-view-status.md)
- [Vytvořit náborové týmy v Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Viz také

- [Vyzkoušejte nebo kupte aplikaci Onboard](https://dynamics.microsoft.com/talent/onboard/)
- [Co je nového a co se změnilo v aplikaci Dynamics 365 Talent](./whats-new.md)
- [Plány vydání](https://docs.microsoft.com/business-applications-release-notes/index)
- [Získání podpory pro Microsoft Dynamics 365 Talent](./talent-support.md)
