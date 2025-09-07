ionic generate page products
ionic generate page product-detail
ionic generate page add-product

<ion-header>
  <ion-toolbar color="primary">
    <ion-title>🛒 المتجر</ion-title>
    <ion-buttons slot="end">
      <ion-button routerLink="/add-product">إضافة منتج</ion-button>
    </ion-buttons>
  </ion-toolbar>
</ion-header>

<ion-content class="ion-padding">
  <ion-list>
    <ion-item *ngFor="let item of products" [routerLink]="['/product-detail', item.id]">
      <ion-thumbnail slot="start">
        <img [src]="item.image" />
      </ion-thumbnail>
      <ion-label>
        <h2>{{ item.name }}</h2>
        <p>{{ item.price }} د.ع</p>
      </ion-label>
    </ion-item>
  </ion-list>
</ion-content>
