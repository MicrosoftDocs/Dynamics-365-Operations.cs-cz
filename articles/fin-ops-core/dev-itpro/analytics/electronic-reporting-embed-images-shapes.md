---
title: Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví
description: Toto téma vysvětluje, jak používat nástroj elektronického výkaznictví (ER) ke generování obchodních dokumentů, které mají vložené obrázky a tvary.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 550ecca31af48e624e292b342d909abd6eb3e87af122f736eb388524b42f1e05
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730628"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Pomocí nástroje elektronického výkaznictví (ER) můžete navrhovat zprávy, které můžete spustit ke generování požadovaných elektronických dokumentů. Můžete použít dokumenty Microsoft Excel nebo Microsoft Word dokumenty k určení rozložení sestavy. Návrhář operací ER umožňuje připojit dokument Excel nebo Word jako šablonu sestavu. Pojmenované prvky v připojené šabloně jsou spojeny s prvky formátu sestavy ER: Prvky formátu sestavy jsou vázány na zdroje dat. Tyto prvky určují data, která budou za běhu zadána do generovaných dokumentů.

Tato nová funkce jde nad rámec stávajících funkcí ER pro vytváření dokumentů ve formátech Microsoft Office. Další informace zjistíte po přehrání následujících průvodců úkoly. Tyto průvodce úkoly najdete v obchodním procesu 7.5.4.3 Získat / vyvinout komponenty IT služeb/řešení (10677).

- Návrh konfigurace ER pro generování sestav ve formátu OPENXML
- Návrh ER konfigurace pro generování sestav ve formátu Microsoft WORD

## <a name="embed-an-image-in-an-excel-document"></a>Vložení obrázku do dokumentu aplikace Excel

### <a name="embed-an-image-in-an-excel-worksheet"></a>Vložení obrázku do listu aplikace Excel

Nejprve musíte přidat zástupný symbol pro obrázek v dokumentu aplikace Excel. Otevřete sešit aplikace Excel a přidejte obrázek jako zástupný symbol pro obrázek, který přidáte později. Poté použijte nástroj ER k přidání nové konfigurace formátu ER tak, aby zahrnovala sestavu, kterou navrhujete. Připojte sešit Excel jako šablonu pro formát sestavy a poté importujte obsah sešitu do formátu ER. Definice formátu bude vytvořena automaticky. Zástupný symbol obrázku, který jste přidali, bude zahrnut do definice formátu ER jako prvek **BUŇKA**.

> [!NOTE]
> Místo importu můžete definici formátu zadat ručně. Když uložíte změny, formát bude ověřen.

Dále spojte prvek **BUŇKA** formátu ER s polem ze zdroje dat formátu, který poskytuje data obrázku v binárním formátu za běhu. Pokud se jako zdroj dat formátu použije datový model ER, musí být datový typ pole [Kontejner](er-formula-supported-data-types-composite.md#container). V současné době pole datového modelu ER, které má datový typ [Kontejner](er-formula-supported-data-types-composite.md#container), lze vázat na několik typů zdrojů dat, které vracejí obrázky v binárním formátu. K poli v datové tabulce a souboru, který je připojen k záznamu datové tabulky, můžete přistupovat pomocí rámce správy dokumentů.

> [!IMPORTANT]
> - Chcete-li vyplnit zástupný symbol obrázku v dokumentu, který vytváříte pomocí šablony aplikace Excel, musí formát ER obsahovat prvek **BUŇKA**, který odkazuje na pojmenovaný prvek obrázku v šabloně aplikace Excel. Jinak se ve výstupu sestavy neobjeví žádný zástupný obrázek. Pokud spojení prvku **BUŇKA** za běhu nevrátí žádná data, generovaný dokument zobrazí zástupný symbol obrázku ze šablony. Chcete-li skrýt obrázek v dokumentu, který generujete, definujte prvek **BUŇKA** a zadejte, že výraz **Povolení** by měl vrátit hodnotu **NEPRAVDA**.
> - V šabloně aplikace Excel použijte pro každý prvek jedinečný název. Mezi tyto prvky patří obrázky a buňky. Pokud duplikujete název prvku, bude obsah generované sestavy nejednoznačný a matoucí.

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Vložte obrázky do záhlaví a zápatí listu aplikace Excel

Pomocí dokumentu sešitu Excel jako šablony můžete určit rozložení sestavy. Sešit může obsahovat více listů, z nichž každý může být navržen tak, aby měl záhlaví a zápatí. Excel podporuje až tři obrázky v záhlaví a zápatí každého listu. Tyto obrázky lze zarovnat doleva, doprava nebo na střed.

Ve verzi Finance 10.0.21 můžete spravovat obrázky záhlaví a zápatí generované řešením ER, které má šablonu aplikace Excel.

Pokud chcete, aby se v záhlaví nebo zápatí vygenerovaného dokumentu zobrazil výchozí obrázek, můžete přidat obrázek do záhlaví nebo zápatí listu šablony ER. Pro přístup k tomuto obrázku ve formátu ER musíte přidat komponentu **Obrázek** pod komponentu [Záhlaví](er-fillable-excel.md#header-component) nebo [Zápatí](er-fillable-excel.md#footer-component) formátu. Nakonfigurujte zarovnání komponenty **Obrázek** podle potřeby. 

Můžete také použít komponenty **Obrázek** pro vložení obrázku do záhlaví nebo zápatí vygenerovaného dokumentu za běhu, i když šablona neobsahuje žádný výchozí obrázek. Chcete-li určit mediální obsah, který by měl být vložen do záhlaví nebo zápatí vygenerovaného dokumentu jako nový obrázek nebo jako náhrada za výchozí obrázek, musíte svázat komponentu **Obrázek** se zdrojem dat typu [Kontejner](er-formula-supported-data-types-composite.md#container), který představuje obrázek v binárním formátu.

Každá komponenta **Záhlaví** nebo **Zápatí** může obsahovat jednu komponentu **Obrázek** pro každé podporované zarovnání: **Doleva**, **Na střed** a **Doprava**.

Vlastnost **Měřítko výšky** komponenty **Obrázek** umožňuje použít nakonfigurovanou vazbu k ovládání velikosti obrázku:

- Vyberte **Původní** k zachování počáteční velikosti obrázku.
- Vyberte **Relativní** ke škálování výšky obrázku v poměru k výšce záhlaví nebo zápatí, ve kterém tento obrázek je.

    - V tomto případě musí být výška obrázku definována jako procento nadřazeného záhlaví nebo zápatí.
    - Pokud hodnota změny měřítka přesáhne 100 procent, může obrázek překrývat datovou oblast příslušného listu.
    - Pokud se při použití změny měřítka změní výška obrazu, změní se také šířka, aby se zachoval původní poměr stran obrazu.

- Vyberte **Absolutní** ke změně velikost obrázku podle hodnot výšky a šířky (v pixelech), které jsou k dispozici v době návrhu.

    - Pokud zadaná výška přesahuje výšku nadřazeného záhlaví nebo zápatí, může obrázek překrývat datovou oblast příslušného listu.

Můžete také použít vlastnost **Povoleno** komponenty **Obrázek** pro řízení viditelnosti obrázku, který je vložen do generovaného dokumentu pomocí této komponenty.

> [!NOTE]
> K přidání komponenty **Obrázek** do upravitelného formátu ER musíte použít návrhář formátu ER. Komponentu nemůžete přidat, když používáte pracovní prostor [Správa obchodních dokumentů](er-business-document-management.md) pro úpravu šablony obchodního dokumentu.

Chcete-li se dozvědět více o této funkci, postupujte podle pokynů v části [Návrh formátu ER pro generování zprávy ve formátu Excel s vloženými obrázky v záhlaví nebo zápatí stránky](er-embed-images-header-footer-excel-reports.md).

## <a name="embed-a-shape-in-an-excel-document"></a>Vložení tvaru do dokumentu aplikace Excel

Nejprve musíte přidat zástupný symbol pro tvar v dokumentu aplikace Excel. Otevřete sešit aplikace Excel a vyberte **Tvar**, **Textové pole** nebo **WordArt** jako zástupný symbol pro tvar. Poté použijte nástroj ER k přidání nové konfigurace formátu ER tak, aby zahrnovala sestavu, kterou navrhujete. Připojte sešit Excel jako šablonu pro formát sestavy a poté importujte obsah sešitu do formátu ER. Definice formátu bude vytvořena automaticky. Zástupný symbol tvaru, který jste přidali, bude zahrnut do definice formátu ER jako prvek **BUŇKA**, který odkazuje na pojmenovaný prvek tvaru aplikace Excel.

> [!NOTE]
> Místo importu můžete definici formátu zadat ručně. Když uložíte změny, formát bude ověřen.

Dále spojte prvek **BUŇKA** ve formátu ER s polem ze zdroje dat formátu, který poskytuje data za běhu. Tato data lze převést na textový řetězec. Když prvek **BUŇKA** ve formátu ER odkazuje na prvek tvaru v šabloně aplikace Excel, který podporuje text, text poskytovaný prostřednictvím této vazby za běhu bude zobrazen ve tvaru v dokumentu, který je generován.

> [!IMPORTANT]
> - Pokud chcete použít šablonu aplikace Excel, která obsahuje zástupný symbol tvaru, ke generování nového dokumentu, musí formát ER obsahovat prvek **BUŇKA**, který odkazuje na prvek tvaru aplikace Excel. Jinak se ve výstupu sestavy neobjeví žádný zástupný tvar. Pokud spojení prvku **BUŇKA**, který odkazuje na pojmenovaný prvek tvaru Excel nevrací za běhu žádná data, generovaný dokument zobrazí text zástupného symbolu tvaru ze šablony aplikace Excel. Chcete-li skrýt tvar v dokumentu, který generujete, definujte prvek **BUŇKA**, který odkazuje na pojmenovaný prvek tvaru Excel, a zadejte, že výraz **Povolení** by měl vrátit hodnotu **NEPRAVDA**.
> - V šabloně aplikace Excel použijte pro každý prvek jedinečný název. Mezi tyto prvky patří tvary a buňky. Pokud duplikujete název prvku, bude obsah generované sestavy nejednoznačný a matoucí.

## <a name="embed-an-image-in-a-word-document"></a>Vložení obrázku do dokumentu aplikace Word
> [!IMPORTANT]
> Můžete znovu použít formát ER, který používá šablonu aplikace Excel k vytváření dokumentů, které obsahují vložené obrázky. Ve formátu ER se ujistěte, že je pro název zadán prvek **BUŇKA** prvek, který odkazuje na pojmenovaný prvek obrázku v aplikaci Excel a který je svázán se zdrojem dat, který vrací obrázek za běhu.

Nejprve musíte nakonfigurovat rozložení dokumentu Word. Použijte ovládací prvek **Obrazový obsah** k vytvoření zástupného symbolu pro vložený obrázek. Chcete-li získat přístup k tomuto ovládacímu prvku, musíte nejprve zviditelnit kartu **Vývojář** na pásu karet aplikace Word.

Dále odstraňte šablonu aplikace Excel z formátu ER a připojte dokument šablony Word. Aktualizujte odkaz na šablonu a uložte změny. Struktura aktuálního formátu ER je uložena do šablony aplikace Word jako nová vlastní část XML s názvem **Sestava**.

Dále uložte šablonu Word pro aktuální formát ER do místního počítače. Otevřete šablonu a otevřete podokno **Mapování XML**. Najděte vlastní část XML s názvem **Zpráva** a pak přejděte na prvek **BUŇKA** v sestavě ER, která je vázána na zdroj dat, který vrací obrázek v binárním formátu. Namapujte položku této části XML na vybraný ovládací prvek **Obrazový obsah** a uložte změny.

[![vložit obrázky.](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

Nakonec odstraňte šablonu Word z formátu ER a připojte dokument Word, který obsahuje namapované vlastní části XML. Aktualizujte odkaz na formát šablony a uložte změny, které jste provedli v tomto formátu ER.

## <a name="more-information"></a>Další informace
Chcete-li se seznámit s podrobnostmi této funkce, přehrajte si sadu průvodců úkoly, **ER Vytváření sestav ve formátech MS Office s vloženými obrázky**. Tito průvodci úkoly ukazují, jak můžete vložit obrázky loga společnosti a podpis oprávněné osoby do platebních šeků, které jsou generovány pomocí nástroje ER v dokumentech Excel a Word.

V následující tabulce jsou uvedeny soubory, které jsou nutné k provedení průvodců úkoly **ER Vytváření sestav ve formátech MS Office s vloženými obrázky** průvodce úkoly. Stáhněte a uložte soubory do místního počítače.

| popis                                          | Název souboru                   |
|------------------------------------------------------|-----------------------------|
| Konfigurace datového modelu elektronického výkaznictví                          | [Model pro cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| Konfigurace formátu elektronického výkaznictví                              | [format.xml pro tisk šeků](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Obrázek loga společnosti                                   | [Company logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Podpisový obrázek                                      | [Signature image.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternativní podpisový obrázek                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Šablona Microsoft Word pro tisk platebních šeků  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| Šablona Microsoft Excel pro tisk platebních šeků | [Cheque template.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

Následující obrázek poskytuje příklad zkušebního výtisku pro platební šek, který je generován z šablony aplikace Excel.

[![Testovací výtisk platebního šeku.](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
