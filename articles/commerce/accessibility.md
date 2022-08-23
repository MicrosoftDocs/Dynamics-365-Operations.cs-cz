---
title: Funkce a možnosti usnadnění přístupu
description: Tento článek obsahuje informace o funkcích a možnostech usnadnění přístupu v různých verzích aplikace Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a797b94d8101100574169cdcecfe8df2b5954c15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278144"
---
# <a name="accessibility-features-and-capabilities"></a>Funkce a možnosti usnadnění přístupu

[!include [banner](includes/banner.md)]

Tento článek obsahuje informace o funkcích a možnostech usnadnění přístupu v různých verzích aplikace Microsoft Dynamics 365 Commerce.

Funkce a možnosti usnadnění přístupu poskytují funkční prostředky pro přístup a provádění akcí, aby mohli všichni uživatelé dosáhnout svých cílů. Tato široká škála uživatelů může vyžadovat pomůcky pro usnadnění sluchu, zraku, mobility nebo neurodiverzity.

Různé funkce v aplikaci Dynamics 365 Commerce umožňují vytvořit web tak, aby zahrnoval asistenční funkce. Při navrhování webu byste měli vzít v úvahu oblasti funkcí usnadnění, které jsou uvedeny v [centru pro usnadnění přístupu společnosti Microsoft](https://www.microsoft.com/accessibility) 

Tento článek popisuje některé další oblasti funkcí usnadnění, které byste měli zvážit při používání Dynamics 365 Commerce.

## <a name="image-alt-text"></a>Alternativní text obrázku

Dynamics 365 Commerce obsahuje integrovaný systém správy digitálních datových zdrojů, který slouží ke sledování datových zdrojů obrazu a videí používaných na vašem webu. Titulky obrázků, popisy a alternativní text lze přidat v podokně vlastností obrázku při jeho výběru nebo odeslání.

## <a name="video-accessibility"></a>Usnadnění přístupu videa

Systém správy digitálního majetku Dynamics 365 Commerce podporuje několik funkcí usnadnění přístupu pro obsah videa. V následující tabulce jsou uvedeny některé příklady.

| Funkce videa               | Popis |
|-----------------------------|-------------|
| Skryté titulky (CC)      | Text, který může být zobrazen pro zvuk a zvukové popisné prvky videa, za účelem pomoci uživatelům s poruchami sluchu |
| Titulky                   | Soubory titulků, které zobrazují text vodítek kontextu nebo dialogu na obrazovce |
| Přepisy zvuku           | Textový přepis mluvených slov, který je generován ze zvuku datového zdroje videa |
| Popisný zvuk           | Neprimární zvukový kanál, který popisuje obsah nebo kontext probíhající na obrazovce |
| Minimální věkové ohraničení            | Atribut, který může uložit minimální věk, který musí mít sledující videa (pouze metadata) |

### <a name="configure-video-accessibility-elements"></a>Konfigurace prvků pro usnadnění přístupu k videu

V aplikaci Commerce v části **Knihovna médií** můžete pro váš web odesílat datové zdroje videa, které mají samostatné soubory pro skryté titulky, běžný zvuk a popisný zvuk. Titulky mohou být také generovány automaticky při odeslání datového zdroje videa.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Generování nebo nahrání souborů skrytých titulků během odesílání videa

Pomocí tohoto kroku postupujte, chcete-li automaticky generovat soubor skrytých titulků při odesílání videa.

- V dialogovém okně **Odesílání datového zdroje** zaškrtněte políčko **Automaticky generovat skryté titulky**. Pokud generujete soubor skrytých titulků, nebude v dialogovém okně k dispozici volič souborů pro soubory skrytých titulků.

Pomocí tohoto kroku postupujte, chcete-li ručně odeslat soubor skrytých titulků při odesílání videa.

- V dialogovém okně **Odesílání datového zdroje** zrušte zaškrtnutí políčka **Automaticky generovat skryté titulky**.

Chcete-li pro video odeslat běžné zvukové nebo popisné zvukové soubory, použijte volič souborů v dialogovém okně **Nahrání datového zdroje**.

> [!NOTE]
> Po odeslání datového zdroje videa lze také přidat skryté titulky, běžný zvuk a popisné zvukové datové zdroje. Přejděte do části **Knihovna médií**, vyberte video a volbou **Upravit** jej rezervujte a pak v podokně vlastností pro datový zdroj videa nahrajte další datové zdroje.

#### <a name="edit-cc-and-audio-transcript-files"></a>Úprava souborů skrytých titulků a přepisu zvuku

Soubory skrytých titulků a přepisu zvuku lze upravovat přímo ve vývojovém nástroji. Přehrávání videa je k dispozici během úprav.

Chcete-li upravit soubory programu skrytých titulků a zvuku, postupujte podle následujících kroků.

1. Přejděte do části **Knihovna médií** a vyberte název souboru datového zdroje videa. Zobrazí se Editor obsahu skrytých titulků a přepisu.
1. Vyberte možnost **Upravit**.
1. Upravte skrytý titulek nebo text přepisu.
1. Po dokončení vyberte **Uložit** a pak **Dokončit úpravy**.
1. Jakmile budete připraveni k publikování, vyberte možnost **Publikovat**.

#### <a name="set-the-minimum-age-attribute"></a>Nastavení atributu minimální věk

Atribut metadat **Minimální věk** může být přidružený k datovým zdrojům videa.

Chcete-li nastavit atribut **Minimální věku** u datového zdroje videa, postupujte následovně.

1. Přejděte do části **Knihovna médií** a vyberte datový zdroj videa.
1. Vyberte možnost **Upravit**.
1. V podokně vlastností datového zdroje videa nastavte atribut **Minimální věk**.

> [!NOTE]
> Podokno vlastností se používá pouze k nastavení a uložení hodnoty atributu metadat. Aby bylo možné použít tento atribut pro přehrávání, musí být vytvořeny přizpůsobené moduly.

## <a name="additional-resources"></a>Další zdroje

[Dostupnost ve formulářích, produktech a ovládacích prvcích](/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Centrum usnadnění společnosti Microsoft](https://www.microsoft.com/accessibility)

[Centrum usnadnění přístupu Dynamics 365](/dynamics365/get-started/accessibility/index)

[Přehled dodržování předpisů](compliance-overview.md)

[Zásady zacházení se soubory cookie](cookie-compliance.md)

[Přidání stránky se zásadami ochrany osobních údajů](add-privacy-page.md)

[Nahrazení ID uživatelů přidružených ke změnám sledovaných obsahů](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
