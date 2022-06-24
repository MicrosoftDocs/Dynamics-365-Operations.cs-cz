---
title: Změna způsobu dodání v POS
description: Tento článek popisuje, jak konfigurovat a používat operaci změny způsobu dodání v POS.
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 583f568164d0de70e22998bf5ded5f4616b00bd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855814"
---
# <a name="change-mode-of-delivery-in-pos"></a>Změna způsobu dodání v POS

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak nastavit a používat funkci „Změnit způsob dodání“ v prostředí pokladního místa (POS). 

V Dynamics 365 Commerce verze 10.0.10 a novějších je k dispozici operace **Změnit způsob dodání** (647), která slouží pro přidání vašich rozložení obrazovky POS.

Funkce změny způsobu dodání umožňuje změnit způsob dodání pro jeden nebo více prodejních řádků konfigurovaných pro dodávku v transakci POS. V předchozích verzích Commerce bylo nutné projít celé toky konfigurace **Odeslat vše** nebo **Odeslat vybrané**, pokud jste chtěli změnit způsob dodání na existujícím řádku nakonfigurovaném pro expedici. Tento proces byl časově náročný a mohl vést k neúmyslným změnám původu dodávky nebo dat dodání pro daný řádek. Nová funkce poskytuje alternativní metodu pro efektivní aktualizaci způsobu dodání na těchto řádcích prodeje.

Další informace, jak přidat operaci k tlačítku v mřížce tlačítek POS, viz [Rozložení obrazovky pokladního místa](pos-screen-layouts.md).

Po konfiguraci této funkce v aplikaci POS se při výběru možnosti **Změnit způsob dodání** zobrazí stránka se seznamem, která vám umožní vybrat řádky transakce, pro které chcete změnit způsob dodání. Můžete vybrat některé nebo všechny řádky nebo ukončit aplikaci bez provedení změn. Řádky prodeje, které byly dříve konfigurovány pro dodávku, jsou jediné řádky v seznamu, které lze změnit. Chcete-li změnit řádek určený k výdeji nebo převzetí a předání k expedici, je nutné použít operace **Odeslat vše** nebo **Odeslat vybrané**. Chcete-li naopak změnit řádek určený jako dodávka k vyzvednutí nebo převzetí, musíte použít operace **Vyzvednout vše**, **Vyzvednout vybrané**, **Převzít vše** nebo **Převzít vybrané**.

Po vybrání řádků, které chcete změnit, klikněte na možnost **Změnit způsob dodání**, abyste mohli vybrat možnosti způsobu dodání. Pokud jste vybrali více řádků, které chcete změnit, zobrazí se v POS pouze způsoby dodání, které byly pro všechny vybrané produkty nakonfigurovány jako povolené. Způsoby dodání lze nakonfigurovat tak, aby podporovaly specifické produkty a dodací adresy. Pokud existuje způsob dodání, který je přijatelný pro jednu kombinaci produktů a adres, ale není přijatelný pro jinou kombinaci vybraného produktu a adresy, není režim dodání k dispozici. Je možné, že budete muset vybrat řádky jeden po druhém a změnit způsob dodání pro každý řádek zvlášť, pokud chcete vybrat způsob dodání pro jeden produkt, který není podporován jiným produktem.  

Po výběru nového způsobu dodání se zobrazí stránka transakce. Chcete-li zkontrolovat nové výběry způsobu dodání, vyberte kartu **Doručení** v seznamu transakcí.

## <a name="additional-resources"></a>Další prostředky

[Vytváření objednávek v kontaktním středisku](tasks/create-call-center-orders.md)

[Přizpůsobení transakčních e-mailů podle způsobu doručení](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]