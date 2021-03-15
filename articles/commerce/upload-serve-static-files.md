---
title: Odeslání a obsluha statických souborů
description: Tohle téma popisuje, jak odeslat statický soubor do konfigurátoru webů Microsoft Dynamics 365 Commerce a jak vytvořit vlastní adresu URL a název souboru, který lze použít k vyžádání tohoto souboru.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1d709d99737ad05af1fb19d9f3ef7b87a8db80d3
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031813"
---
# <a name="upload-and-serve-static-files"></a>Odeslání a obsluha statických souborů

[!include [banner](includes/banner.md)]

Tohle téma popisuje, jak odeslat statický soubor do konfigurátoru webů Microsoft Dynamics 365 Commerce a jak vytvořit vlastní adresu URL a název souboru, který lze použít k vyžádání tohoto souboru.

Některé konektory jiných výrobců vyžadují, aby byl soubor hostován a obsluhován z webu elektronického obchodování. Tyto konektory očekávají, že soubor bude vrácen požadavky na konkrétní cestu URL zpětného volání a název souboru. Toto téma proto vysvětluje, jak nahrát a zobrazit statický soubor, který má na webu uživatelem definovanou adresu URL a název souboru na webu elektronického obchodování Dynamics 365 Commerce.

## <a name="create-a-site-url-that-returns-a-static-file"></a>Vytvoření adresy URL webu, která vrací statický soubor

Chcete-li vytvořit adresu URL webu, která vrací statický soubor v konfigurátoru webů Commerce, postupujte takto.

1. Přejděte do knihovny médií webu a nahrajte soubor, který by měl být obsloužen žádostmi na adresu URL, kterou definujete. Pokud jste již soubor nahráli, můžete tento krok přeskočit.
1. Jděte na **Adresy URL** pro váš web.
1. Zvolte **Nový \> Nová adresa URL**.
1. V dialogovém okně **Nová adresa URL** vyberte **Prostředek knihovny médií**.
1. Do pole **Cesta URL** zadejte cestu URL. Do cesty zahrňte název souboru.
1. Zvolte **Další**. Otevře se knihovna médií a zobrazí se všechny prostředky médií typu **dokument**, které byly nahrány.
1. Vyberte soubor, který má být obsloužen požadavky na adresu URL, kterou jste definovali v kroku 5.
1. Zvolte **Uložit**.

V tomto okamžiku se vytvořená adresa URL nachází ve stavu konceptu. Soubor, na který adresa URL odkazuje, nebude vrácen, dokud adresu URL nepublikujete. Před publikováním adresy URL můžete ověřit, zda vrací správná data.

## <a name="validate-and-publish-a-url"></a>Ověření a publikování adresy URL

Chcete-li ověřit adresu URL před jejím publikování, postupujte takto.

1. Jděte na **Adresy URL** pro váš web a vyberte adresu URL, jejíž náhled chcete zobrazit.
2. V podokně vlastností vpravo pod tlačítkem **Upravit** vyberte správný odkaz na adresu URL. Otevře se nové okno prohlížeče a měla by se zobrazit chyba 404.
3. Připojte řetězec dotazu **?preview=inprogress** k adrese URL (například `https://yoursite.com/callback.html?preview=inprogress`) a znovu načtěte stránku. Soubor, který jste nahráli do knihovny médií, by měl být vrácen v odpovědi.

Po ověření adresy URL ji můžete publikovat.

1. Jděte na **Adresy URL** pro váš web a vyberte adresu URL.
2. Na příkazovém řádku vyberte možnost **Publikovat**.

## <a name="update-the-file-that-a-url-points-to"></a>Aktualizace souboru, na který odkazuje adresa URL

Po publikování adresy URL ji můžete aktualizovat tak, aby odkazovala na jiný soubor. Alternativně můžete adresu URL aktualizovat tak, aby odkazovala na jiný typ prostředku, jak je popsáno v následující části. Můžete například nasměrovat adresu URL na interní stránku nebo přesměrování.

Chcete-li aktualizovat soubor, na který odkazuje adresa URL, postupujte takto.

1. Jděte na **Adresy URL** pro váš web a vyberte adresu URL, kterou chcete aktualizovat.
1. V podokně vlastností vpravo vyberte možnost **Upravit**.
1. V části **Přiřazení adresy URL** vyberte pole **Krok 2** a poté vyberte nový dokument z knihovny médií.
1. Zvolte **Použít**.

## <a name="update-the-asset-type-that-a-url-points-to"></a>Aktualizace typu prostředku, na který odkazuje adresa URL

Můžete také aktualizovat adresu URL tak, aby odkazovala na jiný typ prostředku, například na interní stránku nebo přesměrování.

Chcete-li aktualizovat typ prostředku, na který odkazuje adresa URL, postupujte takto.

1. Jděte na **Adresy URL** pro váš web a vyberte adresu URL, kterou chcete aktualizovat.
1. V podokně vlastností vpravo vyberte možnost **Upravit**.
1. V části **Přiřazení adresy URL** v poli **Krok 1**, vyberte jiný typ prostředku.
1. Vyberte pole **Krok 2** a poté vyberte nový prostředek.
1. Zvolte **Použít**.

## <a name="change-the-url-path"></a>Změna cesty URL

Po vytvoření adresy URL nelze změnit její cestu. Pokud musíte změnit cestu URL, která obsluhuje soubor nebo jiný typ prostředku, musíte vytvořit novou adresu URL, namapovat ji na existující soubor nebo jiný prostředek a poté zrušit publikování a odstranit starou adresu URL.

K úpravě cesty URL postupujte následovně.

1. Chcete-li vytvořit novou adresu URL a namapovat ji na existující soubor nebo jiný prostředek, postupujte podle pokynů v části [Vytvoření adresy URL webu, která vrací statický soubor](#create-a-site-url-that-returns-a-static-file) dříve v tomto tématu.
1. Vyberte novou adresu URL a vyberte **Publikovat** na panelu příkazů. Nová adresa URL je publikována.
1. Chcete-li zrušit publikování staré adresy URL, vyberte ji a poté vyberte **Zrušit publikování** na panelu příkazů. Jestli chcete, můžete nyní odstranit starou adresu URL.

## <a name="additional-resources"></a>Další prostředky

[Přehled správy digitálních aktiv](dam-overview.md)

[Odeslání obrázků](dam-upload-images.md)

[Odeslat videa](dam-upload-video.md)

[Odeslání souborů jiných než obrázky a videa](dam-upload-files.md)

[Oříznutí obrázků](dam-crop-images.md)

[Přizpůsobení ohniska obrázku](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]