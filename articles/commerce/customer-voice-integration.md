---
title: Integrace Customer Voice do stránek webu elektronického obchodu
description: Tento článek popisuje, jak integrovat Microsoft Dynamics 365 Customer Voice do stránek elektronického obchodování Dynamics 365 Commerce.
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: c8c67ecf4950c92fc91c8d119e06e5e8afff0ddf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850323"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>Integrace Customer Voice do stránek webu elektronického obchodu

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak integrovat Microsoft Dynamics 365 Customer Voice do stránek elektronického obchodování Dynamics 365 Commerce.

Můžete integrovat [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) na svůj web elektronického obchodování a shromažďovat, analyzovat a sledovat zpětnou vazbu od zákazníků v reálném čase. Chcete-li začít s integrací, musíte si vytvořit účet a vybrat šablonu projektu Customer Voice pro typ zpětné vazby, kterou chcete shromažďovat.

## <a name="integrate-the-customer-voice-service"></a>Integrujte službu Customer Voice

Chcete-li vytvořit účet Customer Voice, přejděte na [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) a postupujte podle pokynů.

Po vytvoření účtu Customer Voice a přihlášení je dalším krokem výběr šablony projektu pro typ zpětné vazby, kterou chcete shromažďovat.

Chcete-li vybrat šablonu projektu Customer Voice, postupujte takto.

1. Přejděte na [Stránku šablony projektu Customer Voice](https://customervoice.microsoft.com/Pages/ProjectPage.aspx).
1. Vyberte **Začínáme**.
1. Vyberte šablonu projektu pro typ zpětné vazby, kterou chcete shromažďovat, a poté vyberte možnost **Další**.
1. Na kartě **Poslat** v **Vyberte formát pro vložení** vyberte formát pro vložení. Pole **Vložený kód** pole zobrazuje kód, který musí být vložen do konfigurátoru webů Commerce.

Příklady v tomto článku používají šablonu projektu **Pravidelný zákaznický průzkum** a vložený formát **Tlačítko**.

Následující ukázkový obrázek ukazuje stránku šablony projektu **Pravidelný zákaznický průzkum**, kde je vybrána možnost pro formát vložení **Tlačítko** a kód pro vložení pro tuto možnost se zobrazí v poli **Vložený kód**. K vložení poskytnutého kódu na stránky vašeho webu jsou vyžadovány tři samostatné akce, jak je popsáno v následujících částech.

![Stránka pravidelného zákaznického průzkumu Customer Voice s vybranou možností Tlačítko.](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>Vložte adresu URL externího skriptu

Na všechny stránky webu, které by měly mít průzkum Customer Voice, musíte vložit adresu URL externího skriptu, kterou Customer Voice poskytl v kódu pro vložení. Nejlepším způsobem, jak vložit skript na více stránek webu, je vytvořit fragment v nástroji pro tvorbu webu, který obsahuje adresu URL externího skriptu, a poté fragment přidat do příslušných šablon stránek. Po publikování aktualizované šablony bude vložený kód externího skriptu na stránkách takto ošetřených webů vypadat jako následující příklad.

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

Další informace o fragmentech naleznete v tématu [Práce s fragmenty](work-with-fragments.md).

> [!NOTE]
> Musíte pouze přidat adresu URL do fragmentu. Modul externího skriptu přidá další kód skriptu.

Chcete-li vložit adresu URL externího skriptu do fragmentu, postupujte takto.

1. V tvůrci webu vytvořte fragment, který je založen na [Modulu externího skriptu](script-module.md).
1. V novém fragmentu vyberte pozici **Výchozí externí skript**.
1. V podokně vlastností **Výchozí externí skript** v poli **Zdroj skriptu** zadejte adresu URL externího skriptu, jak ukazuje následující příklad.

    ![Adresa URL externího skriptu v poli Zdroj skriptu pro nový fragment.](media/customer-voice-integration-2.png)

1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Vyberte **Publikovat** a publikujte fragment.

Nový fragment, který obsahuje vložený blok externího skriptu, je nyní připraven k přidání do příslušné šablony stránky.

### <a name="embed-the-external-style-sheet-code"></a>Vložte externí kód šablony stylů

Dále na všechny stránky webu, které by měly mít průzkum Customer Voice, musíte vložit externí kód šablony stylů, který Customer Voice poskytl v kódu pro vložení. Stejně jako v předchozí sekci je nejlepším způsobem, jak vložit kód externí šablony stylu na více stránek webu, je vytvořit fragment v nástroji pro tvorbu webu, který obsahuje kód šablony stylů, a poté fragment přidat do příslušných šablon stránek. Vložený kód externí šablony stylů bude připomínat následující příklad kódu.

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

Chcete-li vložit kód externí šablony stylů do fragmentu, postupujte takto.

1. V tvůrci webu vytvořte fragment, který je založen na [Modulu Metaznačky](metatags-module.md).
1. Ve fragmentu vyberte pozici **Výchozí metaznačky**.
1. V podokně vlastností **Výchozí metaznačky** v poli **Metaznačky** zadejte kód šablony stylu, jak ukazuje následující příklad.

    ![Externí kód šablony stylů v poli Meta tagypro nový fragment.](media/customer-voice-integration-3.png)

1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Vyberte **Publikovat** a publikujte fragment.

Nový fragment, který obsahuje vložený kód externí šablony stylů, je nyní připraven k přidání do příslušné šablony stránky.

### <a name="embed-the-inline-script-code"></a>Vložte vložený kód skriptu 

Dále na všechny stránky webu, které by měly mít průzkum Customer Voice, musíte vložit vložený skript, který Customer Voice poskytl v kódu pro vložení. Stejně jako v předchozích sekcích je nejlepším způsobem, jak vložit vložený skript na více stránek webu, je vytvořit fragment v nástroji pro tvorbu webu, který obsahuje kód vloženého skriptu, a poté fragment přidat do příslušných šablon stránek.

V následujícím příkladu kódu vloženého skriptu **SURVEY\_KEY** je zástupný symbol. Hodnota pro **SURVEY\_KEY** by se měl shodovat se skutečným klíčem průzkumu, který Customer Voice poskytl v kódu pro vložení. Poslední řádek volá kód k vykreslení tlačítka průzkumu po jedné sekundě, aby bylo zajištěno, že skripty budou mít dostatek času na načtení. V závislosti na průzkumu, který jste vybrali, možná budete muset přidat nebo aktualizovat další metadata, jako je název společnosti.

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

Chcete-li vložit kód vloženého skriptu do fragmentu, postupujte takto.

1. V tvůrci webu vytvořte fragment, který je založen na [Modulu vloženého skriptu](script-module.md).
1. V novém fragmentu vyberte pozici **Výchozí vložený skript**.
1. V podokně vlastností **Výchozí vložený skript** v poli **Vložený skript** zadejte kód vloženého skriptu, jak ukazuje následující příklad.

    ![Kód vloženého skriptu v poli Vložený skript pro nový fragment.](media/customer-voice-integration-4.png)

1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Vyberte **Publikovat** a publikujte fragment.

Nový fragment, který obsahuje vložený kód vloženého skriptu, je nyní připraven k přidání do příslušné šablony stránky.

## <a name="add-fragments-to-a-template"></a>Přidání fragmentů do šablony

Když dokončíte vytváření fragmentů, které obsahují vložený kód Customer Voice, musíte je přidat do šablon stránek, které jsou přidruženy ke stránkám webu, kde je chcete použít. V následujícím příkladu ilustrace byly tři ukázkové fragmenty přidány do šablony stránky s podrobnostmi o produktu (PDP).

![Příklad fragmentů přidaných do šablony PDP.](media/customer-voice-integration-5.png)

Po publikování aktualizované šablony se průzkum Customer Voice objeví na všech stránkách, které šablona ovládá.

Informace o šablonách získáte v části [Práce s šablonami](work-with-templates.md).

## <a name="configure-content-security-policy"></a>Konfigurace zásad zabezpečení obsahu

Ve výchozím nastavení zásady zabezpečení obsahu (CSP) nepovolují volání jiných služeb, pokud není provedena další konfigurace. Proto po publikování aktualizovaných šablon je pravděpodobné, že se průzkum nepodaří načíst na příslušné stránky webu. Chcete-li zobrazit chyby související s CSP, otevřete vývojářské nástroje webového prohlížeče (F12) a přejděte na stránku s průzkumem. Chyby související s CSP se objeví ve výstupu konzoly.

Chcete-li nakonfigurovat CSP v nástroji pro tvorbu webů a odstranit tak chyby, postupujte takto.

1. Přejděte na **Nastavení webu \> Rozšíření**.
1. Na kartě **Zásady zabezpečení obsahu** přidejte `https://customervoice.microsoft.com/` k předpisu **child-src**.
1. Přidejte `https://customervoice.microsoft.com/` k předpisu **frame-src**.
1. Přidejte `https://mfpembedcdnmsit.azureedge.net` a **.azureedge.net** k předpisu **img-src**.

Další informace viz [Zásady zabezpečení obsahu](manage-csp.md).

## <a name="additional-resources"></a>Další prostředky

[Modul externího skriptu](script-module.md)

[Modul metaznaček](metatags-module.md)

[Modul vloženého skriptu](script-module.md)

[Zásady zabezpečení obsahu](manage-csp.md)

[Práce s fragmenty](work-with-fragments.md)

[Práce se šablonami](work-with-templates.md)
