import cv2

# Load the image of an apple
image_path = "apple.jpg"  # Replace with your image file path
img = cv2.imread(image_path)

# Check if the image was successfully loaded
if img is None:
    print(f"Error: Unable to load image '{image_path}'.")
else:
    # Define rectangle parameters (coordinates, size, color)
    start_point = (30, 10)  # (x, y) starting point of the rectangle
    end_point = (330, 355)   # (x, y) ending point of the rectangle
    color = (10, 88, 53)      # BGR color format: (Blue, Green, Red)
    thickness = 3           # Thickness of the rectangle border (in pixels)

    # Draw rectangle on the image
    img_with_rectangle = cv2.rectangle(img, start_point, end_point, color, thickness)

    # Display the modified image with rectangle
    cv2.imshow("Image with Rectangle", img_with_rectangle)
    cv2.waitKey(0)  # Wait for any key press to close the image window
    cv2.destroyAllWindows()
