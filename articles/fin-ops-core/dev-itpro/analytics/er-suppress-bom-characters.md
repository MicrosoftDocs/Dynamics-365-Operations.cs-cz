---
title: Návrh konfigurací ER k potlačení znaků kusovníku ve vygenerovaných souborech
description: Tento článek vysvětluje, jak nakonfigurovat formát elektronického výkaznictví (ER) pro generování sestav, které potlačují znaky značka pořadí bajtů (BOM).
author: kfend
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: EROperationDesigner
ms.openlocfilehash: a2ea132b51f2f451fbe81a9c7869bea84bf4017a
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324012"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>Návrh konfigurací ER k potlačení znaků kusovníku ve vygenerovaných souborech

[!include [banner](../includes/banner.md)]

Můžete navrhnout [řešení](general-electronic-reporting.md) [pro formát elektronického výkaznictví (ER)](er-quick-start1-new-solution.md) ke generování odchozích dokumentů. Chcete-li generovat dokumenty jako textové nebo XML soubory, musí řešení obsahovat [konfiguraci](general-electronic-reporting.md#Configuration) ER, která obsahuje komponentu formátu ER. Chcete-li určit [kódování znaků](/windows/win32/intl/character-sets), které představuje sadu znaků v generovaných souborech, musí formát ER obsahovat prvek formátu **Běžný\\Soubor**. Chcete-li nakonfigurovat komponentu formátu ER, musíte otevřít rámcovou verzi konfigurace ER v návrháři formátu ER a přidat prvek **Společné\\Soubor**. V poli **Kódování** zadejte kódování odchozích souborů generovaných za běhu pomocí této komponenty.

> [!NOTE]
> Pokud formát obsahuje nesprávný název kódování, dojde k chybě, když uložíte změny v nastavení formátu.

![Přidání kořenového prvku a polí na stránce Návrhář formátu.](./media/er-suppress-bom-characters-image1.gif)

Pokud jako kódování zadáte **UTF-8**, **UTF-16**, nebo **UTF-32**, zpřístupní se možnost **Potlačit znaky BOM**. Tuto možnost nastavte na **Ano**, pokud chcete potlačit [znaky pořadí bajtů (BOM)](/globalization/encoding/byte-order-mark) v odchozích souborech, které jsou generovány za běhu, když je spuštěn upravitelný formát ER.

> [!NOTE]
> Ponecháte-li pole **Kódování** prázdné, použije se výchozí kódování **UTF-8**.

![Nastavení možnosti Potlačit znaky BOM na stránce Návrhář formátů.](./media/er-suppress-bom-characters-image2.gif)

Chcete-li zkontrolovat funkčnost za běhu, proveďte příslušný postup. Například proveďte kroky v článku [Odložit provedení prvků XML ve formátech ER](er-defer-xml-element.md). Po dokončení kroků v části [Úprava formátu tak, aby byl výpočet založen na generovaném výstupu](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) tohoto článku, postupujte podle těchto dalších kroků.

1. Zadejte kódování UTF:

    1. vyberte prvek **Report** typu **Common\\File**.
    2. Do pole **Kódování** zadejte kódování **UTF-8**.

2. Vygenerujte soubor XML, který obsahuje znak BOM:

    1. Nastavte možnost **Potlačit znaky BOM** na **Ne**, pokud chcete zahrnout znaky BOM do vygenerovaných souborů XML.
    2. Proveďte kroky v části [Odložit provedení souhrnného prvku XML tak, aby se použil vypočítaný součet](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) článku [Odložení provedení prvků XML ve formátech ER](er-defer-xml-element.md) a uložte vygenerovaný soubor jako **SampleXmlReport.xml**.

3. Vygenerujte soubor XML, který neobsahuje znak BOM:

    1. Nastavte možnost **Potlačit znaky BOM** na **Ano**, pokud chcete potlačit znaky BOM do vygenerovaných souborů XML.
    2. Proveďte kroky v části [Odložit provedení souhrnného prvku XML tak, aby se použil vypočítaný součet](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) článku [Odložení provedení prvků XML ve formátech ER](er-defer-xml-element.md) a uložte vygenerovaný soubor jako **SampleXmlReport (1).xml**.

4. V nástroji pro porovnávání souborů porovnejte vygenerované soubory.

    První rozdíl, kterého si všimnete, je v záhlaví souboru. Soubor SampleXmlReport.xml obsahuje znak BOM, kdežto soubor SampleXmlReport (1) .xml nikoli.

    ![Porovnávání generovaných souborů pomocí nástroje pro porovnání souborů.](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>Viz také

- [Odložení provádění prvků XML ve formátech elektronického výkaznictví](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
