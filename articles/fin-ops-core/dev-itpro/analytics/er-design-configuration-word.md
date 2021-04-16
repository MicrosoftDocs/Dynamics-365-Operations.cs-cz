---
title: Návrh nové konfigurace ER pro generování sestav ve formátu Word
description: Toto téma vysvětluje, jak mohou uživatelé konfigurovat nový formát elektronického výkaznictví (ER) pro generování sestav jako dokumentů Microsoft Word.
author: NickSelin
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 4885caf017fa0f9d36d293fa32aad53c21d3f162
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753569"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>Návrh nové konfigurace ER pro generování sestav ve formátu Word

[!include [banner](../includes/banner.md)]

Abyste mohli generovat zprávy jako dokumenty Microsoft Word, musíte navrhnout šablonu pro zprávy například pomocí desktopové aplikace Word. Následující obrázek ukazuje vzorovou šablonu pro kontrolní sestavu, kterou lze vygenerovat pro zobrazení podrobností zpracovaných plateb dodavatele.

![Ukázková šablona pro kontrolní sestavu v desktopové aplikaci Word](./media/er-design-configuration-word-image1.png)

Chcete-li použít dokument Word jako šablonu pro sestavy ve formátu Word, můžete nakonfigurovat nové [řešení](general-electronic-reporting.md)[elektronického výkaznictví (ER)](er-quick-start1-new-solution.md). Toto řešení musí obsahovat [konfiguraci ER](general-electronic-reporting.md#Configuration), která obsahuje komponentu [formát](general-electronic-reporting.md#FormatComponentOutbound) ER.

> [!NOTE]
> Když vytvoříte novou konfiguraci formátu ER pro generování sestav ve formátu Word, musíte jako typ formátu zdroje vybrat buď **Word** v rozevíracím dialogu **Vytvořit konfiguraci**, nebo nechat pole **Typ formátu** prázdné.

![Vytvoření konfigurace formátu na stránce Konfigurace](./media/er-design-configuration-word-image2.gif)

Komponenta formátu ER řešení musí obsahovat prvek formátu **Excel\\Soubor** a tento prvek formátu musí být propojen s dokumentem Word, který bude použit jako šablona pro generované sestavy za běhu. Chcete-li nakonfigurovat komponentu formátu ER, musíte otevřít [rámcovou](general-electronic-reporting.md#component-versioning) verzi vytvořené konfigurace ER v návrháři formátu ER. Pak přidejte prvek **Excel\\Soubor**, připojte šablonu Wordu k upravitelnému formátu ER a propojte tuto šablonu s prvkem **Excel\\Soubor**, který jste přidali.

> [!NOTE]
> Když ručně připojíte šablonu, musíte použít [typ dokumentu](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), který byl předtím [nakonfigurován](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) v parametrech ER k uložení šablon formátů ER.

![Připojení šablony na stránce Návrhář formátů](./media/er-design-configuration-word-image3.gif)

Můžete přidat vnořené prvky **Excel\\Rozsah** a **Excel\\Buňka** pro prvek **Excel\\Soubor** k určení struktury dat, která budou zadána do generovaných sestav za běhu. Tyto prvky pak musíte vázat se zdroji dat upravitelného formátu ER, abyste určili skutečná data, která budou zadána do generovaných sestav za běhu.

![Přidání vnořených prvků a polí na stránce Návrhář formátu](./media/er-design-configuration-word-image4.gif)

Když uložíte změny do formátu ER v době návrhu, hierarchická struktura formátu se uloží v přiložené šabloně Word jako [vlastní část XML](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), která má název **Sestava**. Musíte mít přístup k upravené šabloně, stáhnout ji z aplikace Finance, uložit ji místně a otevřít ji v desktopové aplikaci Word. Následující obrázek ukazuje lokálně uloženou ukázkovou šablonu pro kontrolní sestavu, která obsahuje vlastní část XML **Sestava**.

![Náhled ukázkové šablony sestavy v desktopové aplikaci Word](./media/er-design-configuration-word-image5.gif)

Při vázání prvků formátu **Excel\\Rozsah** a **Excel\\buňka** v době běhu jsou data, která každá vazba doručí, v generovaném dokumentu Word jako jednotlivé pole části vlastního XML **Sestava**. Chcete-li do generovaného dokumentu zadat hodnoty z polí vlastní části XML, musíte přidat příslušné [ovládací prvky obsahu](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) aplikace Word do šablony aplikace Word, aby sloužil jako zástupný symbol pro data, která budou vyplněna za běhu. Chcete-li určit, jak se vyplňují ovládací prvky obsahu, namapujte každý ovládací prvek obsahu do příslušné vlastní části XML **Sestavy** .

![Přidávání a mapování ovládacích prvků obsahu v desktopové aplikaci Word](./media/er-design-configuration-word-image6.gif)

Poté musíte nahradit původní šablonu Word upravitelného formátu ER upravenou šablonou, která nyní obsahuje ovládací prvky obsahu Word, které byly namapovány na vlastní část XML pole **Sestava**.

![Nahrazení šablony na stránce Návrhář formátů](./media/er-design-configuration-word-image7.gif)

Když spustíte nakonfigurovaný formát ER, připojená šablona Word se použije ke generování nové sestavy. Skutečná data jsou uložena v sestavě Word jako vlastní část XML s názvem **Sestava**. Po otevření vygenerované sestavy se ovládací prvky obsahu Word vyplní údaji z vlastní části XML **Sestavy**.

## <a name="frequently-asked-questions"></a>Časté dotazy

**Otázka:** Nakonfiguroval jsem formát ER pro tisk dokumentu Word, který obsahuje adresu společnosti. Do šablony Word pro tento formát ER jsem vložil ovládací prvek obsahu ve formátu RTF představující adresu společnosti. V sekci Finance jsem zadal adresu společnosti jako víceřádkový text a vybral **Enter** pro přidání přesunu na nový řádek pro každý řádek, který jsem zadal. Proto očekávám, že se adresa společnosti v generovaných dokumentech zobrazí jako víceřádkový text. Adresa se však zobrazí jako jeden řádek textu, který místo návratových hodnot obsahuje speciální symboly. Co je na mém nastavení špatně?

**Odpověď:** Místo použití ovládacího prvku obsahu ve formátu RTF musíte použít ovládací prvek obsahu ve formátu prostého textu a zaškrtnout políčko **Povolit posun na nový řádek (více odstavců)** ve vlastnostech ovládacího prvku.

## <a name="additional-resources"></a>Další prostředky

- [Opětovné použití konfigurace ER se šablonami aplikace Excel ke generování zpráv ve formátu Word](./tasks/er-design-configuration-word-2016-11.md)
- [Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]