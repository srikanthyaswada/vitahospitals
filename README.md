<!-- how to open search box dropdown -->
[3:23 pm, 03/04/2024] +91 96763 43074: npm install @fortawesome/fontawesome-free@5.15.3
[3:24 pm, 03/04/2024] +91 96763 43074: <div class="container mt-5">
  <!-- Search Icon -->
  <button class="btn btn-primary" (click)="toggleSearch()">
    <i [ngClass]="searchIcon"></i>
  </button>
  
  <!-- Search Box -->
  <div class="search-box mt-3" [hidden]="!isSearchOpen">
    <input type="text" class="form-control" placeholder="Search...">
  </div>
</div>
[3:25 pm, 03/04/2024] +91 96763 43074: import { Component } from '@angular/core';

@Component({
  selector: 'app-search-box',
  templateUrl: './search-box.component.html',
  styleUrls: ['./search-box.component.css']
})
export class SearchBoxComponent {
  isSearchOpen: boolean = false;
  searchIcon: string = 'fas fa-search'; // Initial icon class

  toggleSearch() {
    this.isSearchOpen = !this.isSearchOpen;
    // Change icon from search to close and vice versa
    this.searchIcon = this.isSearchOpen ? 'fas fa-times' : 'fas fa-search';
  }
}